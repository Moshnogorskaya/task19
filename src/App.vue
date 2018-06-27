<template>
  <div class="app">
    <div class='wrapper'>
      <navigation />
      <keep-alive>
        <router-view @gotFreshRepos='repos = $event' :repos='repos' />
      </keep-alive>
    </div>
    <footer-info />
  </div>
</template>

<script>

import Navigation from '@/components/header/Navigation.vue';
import FooterInfo from '@/components/FooterInfo.vue';

export default {
  name: 'app',
  components: {
    Navigation,
    FooterInfo,
  },
  data() {
    return {
      repos: {},
    };
  },
};
</script>


<style>
body {
  margin: 0;
  padding: 0;
  min-width: 1000px;
  font-family: Roboto, sans-serif;
}

div,
a,
h1,
p,
ul,
li,
form,
input,
select,
button {
  padding: 0;
  margin: 0;
  display: flex;
  box-sizing: border-box;
  border: none;
  border-radius: 0px;
  appearance: none;
}

.app {
  flex-direction: column;
  align-items: center;
  width: 100%;
  min-height: 100vh;
}

.wrapper {
    flex: 1;
    flex-direction: column;
    align-items: center;
    width: 100%;
}
</style>
