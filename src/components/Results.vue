<template>
<div class='results'>
   <!-- <results-list /> -->
   <results-dashboard />
   <!-- <no-results /> -->
   </div>
</template>

<script>

import ResultsList from '@/components/list/ResultsList.vue';
import ResultsDashboard from '@/components/dashboard/ResultsDashboard.vue';
import NoResults from './NoResults.vue';

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
