<template>
  <div class="my-list">
    <h1 class="my-list__heading">My List</h1>
    <results v-if='repos.length'/>
    <no-results v-else />
  </div>
</template>

<script>
import Results from '@/components/Results.vue';
import NoResults from '@/components/NoResults.vue';

export default {
  name: 'my-list',
  components: {
    Results,
    NoResults,
  },
  data() {
    return {
      repos: [1],
    };
  },
};
</script>

<style>
.my-list {
  flex-direction: column;
  width: 80%;
  align-items: center;
}
.my-list__heading {
  height: 60px;
  font-weight: normal;
  justify-content: flex-start;
  width: 100%;
  padding-top: 30px;
}
</style>
