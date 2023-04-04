<template>
  <div class="card">
    <div class="card__image">
      <img :src="imagePath" :alt="title" />
    </div>
    <h2 class="card__title">{{ title }}</h2>
    <div class="card__actions">
      <div class="card__action">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="card__action-icon">
          <path
            d="M11.644 1.59a.75.75 0 01.712 0l9.75 5.25a.75.75 0 010 1.32l-9.75 5.25a.75.75 0 01-.712 0l-9.75-5.25a.75.75 0 010-1.32l9.75-5.25z" />
          <path
            d="M3.265 10.602l7.668 4.129a2.25 2.25 0 002.134 0l7.668-4.13 1.37.739a.75.75 0 010 1.32l-9.75 5.25a.75.75 0 01-.71 0l-9.75-5.25a.75.75 0 010-1.32l1.37-.738z" />
          <path
            d="M10.933 19.231l-7.668-4.13-1.37.739a.75.75 0 000 1.32l9.75 5.25c.221.12.489.12.71 0l9.75-5.25a.75.75 0 000-1.32l-1.37-.738-7.668 4.13a2.25 2.25 0 01-2.134-.001z" />
        </svg>
        <a class="card__action-link" href="#">View Study Case</a>
      </div>
      <!--  -->
      <div class="card__action">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="card__action-icon">
          <path d="M12 15a3 3 0 100-6 3 3 0 000 6z" />
          <path fill-rule="evenodd"
            d="M1.323 11.447C2.811 6.976 7.028 3.75 12.001 3.75c4.97 0 9.185 3.223 10.675 7.69.12.362.12.752 0 1.113-1.487 4.471-5.705 7.697-10.677 7.697-4.97 0-9.186-3.223-10.675-7.69a1.762 1.762 0 010-1.113zM17.25 12a5.25 5.25 0 11-10.5 0 5.25 5.25 0 0110.5 0z"
            clip-rule="evenodd" />
        </svg>

        <a class="card__action-link" href="#">Live Preview</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imagePath: { required: true, type: String },
    title: { required: true, type: String }
  }
}
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  /* width: 50rem; */
}

.card__image {
  margin-bottom: 3rem;
}

.card__image img {
  width: 100%;
  border-radius: 2.5rem;
  aspect-ratio: 3/2;
}

.card__title {
  font-weight: 600;
  font-size: 2.4rem;
  line-height: 3.6rem;
  color: #1c1c1c;
  margin-bottom: 1rem;
}

.card__actions {
  display: flex;
  align-items: center;
  gap: 4rem;
}

.card__action {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
}

.card__action-icon {
  width: 1.8rem;
  height: 1.8rem;
  cursor: pointer;
}

.card__action-link {
  text-decoration: none;
  font-weight: 500;
  font-size: 1.6rem;
  line-height: 2.4rem;
  color: #151517;
}
</style>
