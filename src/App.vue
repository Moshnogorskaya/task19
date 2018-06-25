<template>
  <div class="app">
    <navigation />
    <router-view/>
    <div class='footer'>Footer</div>
  </div>
</template>

<script>

import Navigation from '@/components/Navigation.vue';

export default {
  name: 'app',
  components: {
    Navigation,
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
}

</style>
