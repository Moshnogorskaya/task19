<template>
<ul class="results-list">
        <li v-for='(value, key) in repos' :key='key' class="results-list__item">
          <list-view :repo='value' />
        </li>
    </ul>
</template>

<script>

import ListView from './ListView.vue';

export default {
  name: 'results',
  props: ['repos'],
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
