<template>
<div class='results'>
   <results-list />
   <!-- <results-dashboard /> -->
   </div>
</template>

<script>

import ResultsList from '@/components/list/ResultsList.vue';
import ResultsDashboard from '@/components/dashboard/ResultsDashboard.vue';

export default {
  name: 'results',
  components: {
    ResultsList,
    ResultsDashboard,
  },
  // data: function() {
  //   return {
  //     isList: true,
  //   }
  // },
  // methods: {
  //   toggle: function() {
  //     this.isList = !this.isList;
  //   }
  // },
};
</script>

<style>
.results {
    flex-direction: column;
    width: 100%;
    align-items: center;
}
</style>
