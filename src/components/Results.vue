<template>
<div class='results'>
   <!-- <results-list /> -->
   <results-dashboard />
   <!-- <no-results /> -->
   </div>
</template>

<script>

import NoResults from '@/components/NoResults.vue';
import ResultsList from '@/components/ResultsList.vue';
import ResultsDashboard from '@/components/ResultsDashboard.vue';


export default {
  name: 'results',
  components: {
    NoResults,
    ResultsList,
    ResultsDashboard,
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
