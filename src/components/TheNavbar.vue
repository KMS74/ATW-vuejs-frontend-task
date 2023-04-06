<template>
  <nav class="navbar">
    <div class="navbar__logo">LOGO</div>
    <ul class="navbar__list" :class="{ 'nav-open': mobileNav, 'scale-up-center': mobileNav }">
      <li class="navbar__list-item">
        <RouterLink v-on:click="hideMobileNav" class="navbar__nav-link" to="/">Home</RouterLink>
      </li>
      <li class="navbar__list-item">
        <RouterLink v-on:click="hideMobileNav" class="navbar__nav-link" to="/about"
          >About</RouterLink
        >
      </li>
      <li class="navbar__list-item">
        <RouterLink v-on:click="hideMobileNav" class="navbar__nav-link" to="/projects"
          >Projects</RouterLink
        >
      </li>
      <li class="navbar__list-item">
        <RouterLink v-on:click="hideMobileNav" class="navbar__nav-link" to="/contact"
          >Contact</RouterLink
        >
      </li>
    </ul>
    <!-- Mobile Nav Open/Close Icons -->
    <button class="navbar__mobile-icons">
      <!-- Hamburger Icon -->
      <svg
        v-if="!mobileNav"
        v-on:click="showMobileNav"
        xmlns="http://www.w3.org/2000/svg"
        class="navbar__mobile-icon navbar__mobile-icon--open"
        width="32"
        height="32"
        fill="#2f2f2f"
        viewBox="0 0 256 256"
      >
        <path
          d="M224,128a8,8,0,0,1-8,8H40a8,8,0,0,1,0-16H216A8,8,0,0,1,224,128ZM40,72H216a8,8,0,0,0,0-16H40a8,8,0,0,0,0,16ZM216,184H40a8,8,0,0,0,0,16H216a8,8,0,0,0,0-16Z"
        ></path>
      </svg>
      <!-- Close Icon -->
      <svg
        v-if="mobileNav"
        v-on:click="hideMobileNav"
        xmlns="http://www.w3.org/2000/svg"
        class="navbar__mobile-icon navbar__mobile-icon--close"
        width="32"
        height="32"
        fill="#2f2f2f"
        viewBox="0 0 256 256"
      >
        <path
          d="M205.66,194.34a8,8,0,0,1-11.32,11.32L128,139.31,61.66,205.66a8,8,0,0,1-11.32-11.32L116.69,128,50.34,61.66A8,8,0,0,1,61.66,50.34L128,116.69l66.34-66.35a8,8,0,0,1,11.32,11.32L139.31,128Z"
        ></path>
      </svg>
    </button>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      mobileNav: false
    }
  },
  methods: {
    showMobileNav() {
      this.mobileNav = true
    },
    hideMobileNav() {
      this.mobileNav = false
    }
  }
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.6rem 9.6rem;
  margin-bottom: 1.6rem;
  position: relative;
}

.navbar__logo {
  font-weight: 700;
  font-size: 2.2rem;
  line-height: 3.3rem;
  color: #151517;
}

.navbar__list {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 4rem;
}

.navbar__nav-link:link,
.navbar__nav-link:visited {
  text-decoration: none;
  font-weight: 500;
  font-size: 1.8rem;
  line-height: 2.4rem;
  color: #2f2f2f;
  transition: 0.3s all;
}

.navbar__nav-link:hover,
.navbar__nav-link.router-link-active {
  color: #eebf63;
}

/* MOBILE  NAV*/
.navbar__mobile-icons {
  border: none;
  background: none;
  cursor: pointer;
  /* By default hidden */
  display: none;
}

@media (max-width: 670px) {
  .navbar {
    padding: 1.6rem 3.2rem;
    background-color: #eebf63;
  }

  .navbar__mobile-icons {
    display: block;
    z-index: 999;
  }

  .navbar__list {
    /* Hide Navigation correctly */
    /* 1) Hide it visually */
    opacity: 0;
    /* Make it unaccessible to mouse and keyboard */
    pointer-events: none;
    /* Hide it from screan readers */
    visibility: hidden;
    display: none;
  }

  .navbar__list.nav-open {
    /* Show Mobile Nav */
    opacity: 1;
    pointer-events: auto;
    visibility: visible;

    display: flex;
    flex-direction: column;
    gap: 4rem;
    padding: 1rem;
    position: absolute;
    top: 60px;
    right: 50px;
    margin-top: 1rem;
    min-width: 200px;
    border-radius: 5px;
    box-shadow: 0 0 16px rgba(17, 17, 26, 0.1);
  }
}

@media (max-width: 450px) {
  .navbar__list.nav-open {
    min-width: 140px;
    top: 60px;
    right: 40px;
  }
}
</style>
