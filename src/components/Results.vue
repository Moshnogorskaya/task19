<template>
<div class='results'>
   <results-list />
   <!-- <div>Results-dashboard</div> -->
   <!-- <no-results /> -->
   </div>
</template>

<script>

import NoResults from '@/components/NoResults.vue';
import ResultsList from '@/components/ResultsList.vue';

export default {
  name: 'results',
  components: {
    NoResults,
    ResultsList,
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
