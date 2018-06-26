<template>
<ul class="results-list">
        <li class="results-list__item">
          <list-view />
        </li>
         <li class="results-list__item">
          <list-view />
        </li>
         <li class="results-list__item">
          <list-view />
        </li>
         <li class="results-list__item">
          <list-view />
        </li>
         <li class="results-list__item">
          <list-view />
        </li>
    </ul>
</template>

<script>

import ListView from '@/components/ListView.vue';

export default {
  name: 'results',
  components: {
    ListView,
  },
};
</script>

<style>
.results-list {
  flex-direction: column;
  width: 100%;
}

.results-list__item {
  height: 147px;
  border-top: 1px solid #e1e4e8;
}
</style>
