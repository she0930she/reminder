<template>
  <div>
    <div class="container">
      <!-- TODO: navbar-->
      <!-- navbar -->
      <NavBar />
      <!-- navbar END-->
      <div>
        <!-- <nuxt-link to="/">BMP</nuxt-link>
      <nuxt-link to="/customer">customer</nuxt-link>
      <nuxt-link to="">office</nuxt-link> -->
        <h1>{{ title }}</h1>
        <input type="text" v-model="title" />
      </div>

      <!-- <div>
      <Logo />
      <h1 class="title">reminder</h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div> -->
    </div>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar";
export default {
  name: "indexPage",
  components: {
    NavBar,
  },
  data() {
    return {
      title: "Home",
    };
  },
};
</script>

<style>
/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
