<template>
  <div>
    <nav>
      <nuxt-link to="/">BMP</nuxt-link>
      <nuxt-link to="/office">office</nuxt-link>
      <nuxt-link to="/customer">客戶管理</nuxt-link>
      <button>SignIn</button>
    </nav>
  </div>
</template>
<script>
export default {
  name: "NavBar",
  props: {},
};
</script>