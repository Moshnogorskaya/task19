<template>
  <div class="app">
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
}

</style>
