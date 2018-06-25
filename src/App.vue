<template>
  <div id="app">
    <Header />
    <router-view/>
    <div class='footer'>Footer</div>
  </div>
</template>

<script>

import Header from '@/components/Header.vue';

export default {
  name: 'app',
  components: {
    Header,
  },
};
</script>


<style>
</style>

<!--
<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Search</router-link> |
      <router-link to="/my-list">My List</router-link>
    </div>
    <router-view/>
  </div>
</template>
-->
