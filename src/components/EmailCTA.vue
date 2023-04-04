<template>
  <div class="cta">
    <p class="cta__text">Interested working with me?</p>
    <button class="cta__btn">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor"
        class="cta__btn-icon">
        <path stroke-linecap="round" stroke-linejoin="round"
          d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
      </svg>

      <span class="cta__btn-text">Email Me</span>
    </button>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.cta {
  background-color: #eebf63;
  padding: 4.2rem 5.6rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-radius: 2.5rem;
  margin-bottom: 18rem;
}

.cta__text {
  font-weight: 600;
  font-size: 4.5rem;
  flex: 0.6;
  line-height: 6.2rem;
  color: #fff;
}

.cta__btn {
  display: flex;
  gap: 1.6rem;
  align-items: center;
  background: #fff;
  box-shadow: 0px 0.927421px 1.92354px rgba(0, 0, 0, 0.00974257);
  border: none;
  outline: none;
  border-radius: 1rem;
  padding: 0.8rem 3.6rem;
  cursor: pointer;
}

.cta__btn-text {
  font-weight: 600;
  font-size: 1.8rem;
  line-height: 3.6rem;
  color: #2f2f2f;
}

.cta__btn-icon {
  width: 2.5rem;
  height: 2.5rem;
  color: #2f2f2f;
}

@media (max-width: 980px) {
  .cta__text {
    flex: 0.7;
  }
}

@media (max-width: 850px) {
  .cta {
    flex-direction: column;
    justify-content: center;
    gap: 2rem;
    text-align: center;
    padding: 2.4rem;

  }

  .cta__text {
    font-size: 3rem;
  }
}
</style>
