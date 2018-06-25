<template>
  <div id="app">
    <div class='header'>
      <router-link to="/">Search</router-link>
      <router-link to="/my-list">My List</router-link>
    </div>
    <router-view/>
    <div class='footer'>Footer</div>
  </div>
</template>

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
