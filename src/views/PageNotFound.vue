<template>
  <div class="pageNotfound">
    <h1>404 ERROR.</h1>
    <p>Oooooops! Looks like nothing was found at this location. Maybe try on of the links below?</p>
    <router-link to="/">Let's Get you home!</router-link>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.pageNotfound {
  background-image: url(../assets/img/greens.jpg);
  background-repeat: no-repeat;
  background-position: center;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  background-size: cover;
  height: 100vh;
  width: 100vw;
  text-align: center;
  color: aliceblue;
}

h1 {
  font-family: "roboto-black", sans-serif;
  text-transform: uppercase;
  letter-spacing: -0.2rem;
  font-size: 9.4rem;
  line-height: 1;
  margin-bottom: 1.2rem;
  padding-top: 2.4rem;
  position: relative;
}

p {
  font-size: 50px;
  font-weight: 100;
}
</style>
