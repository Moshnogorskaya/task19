<template>
  <div class="search">
    <search-panel />
    <results />
    <!-- <no-results /> -->
  </div>
</template>

<script>

import SearchPanel from '@/components/searchPanel/SearchPanel.vue';
import Results from '@/components/Results.vue';
import NoResults from '@/components/NoResults.vue';

export default {
  name: 'search',
  components: {
    SearchPanel,
    Results,
    NoResults,
  },
};
</script>

<style>
.search {
  flex-direction: column;
  align-items: center;
  width: 80%;
}

</style>
