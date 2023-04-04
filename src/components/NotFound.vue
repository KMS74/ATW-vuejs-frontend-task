<template>
  <div class="not-found">
    <div class="not-found__img">
      <img src="../assets/images/404 Error Page not Found.png" alt="">
    </div>
    <RouterLink to="/projects" class="not-found__btn">Go Home</RouterLink>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.not-found {
  margin-bottom: 4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.not-found__img {
  /* width: 50%; */
  display: flex;
  justify-content: center;
}

.not-found__img img {
  width: 50%;
}


.not-found__btn {
  color: #333;
  font-weight: 500;
  text-decoration: none;
  font-size: 1.8rem;
  background: #eebf63;
  box-shadow: 0px 0.927421px 1.92354px rgba(0, 0, 0, 0.00974257);
  border: none;
  outline: none;
  border-radius: 1rem;
  padding: 0.8rem 3.6rem;
  cursor: pointer;
}
</style>
