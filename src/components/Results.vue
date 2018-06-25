<template>
<div class='results'>
   <!-- <div>Results-list</div>
   <div>Results-dashboard</div> -->
   <no-results />
   </div>
</template>

<script>

import NoResults from '@/components/NoResults.vue';

export default {
  name: 'results',
  components: {
    NoResults,
  },
};
</script>

<style>
.results {
    flex-direction: column;
    width: 100%;
    align-items: center;
}
</style>
