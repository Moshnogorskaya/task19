<template>
  <div class="search">
    <search-panel />
    <toggle-view />
    <results />
  </div>
</template>

<script>

import SearchPanel from '@/components/searchPanel/SearchPanel.vue';
import ToggleView from '@/components/ToggleView.vue';
import Results from '@/components/Results.vue';

export default {
  name: 'search',
  components: {
    SearchPanel,
    ToggleView,
    Results,
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

