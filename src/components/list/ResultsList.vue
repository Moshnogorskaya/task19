<template>
  <ul class="results-list">
    <li v-for='(value, key) in repos' :key='key' class="results-list__item">
      <div class="repo">
        <div class="wrapper-repo-action">
          <button class='repo__action' />
        </div>
        <list-view-info :repo='value' />
        <list-view-stats :repo='value' />
      </div>
    </li>
  </ul>
</template>

<script>

import ListViewInfo from './ListViewInfo.vue';
import ListViewStats from './ListViewStats.vue';

export default {
  name: 'results',
  props: ['repos'],
  components: {
    ListViewInfo,
    ListViewStats,
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
.repo {
  width: 100%;
}
.wrapper-repo-action {
  padding-top: 32px;
}
.repo__action {
  outline: 1px solid #0366d6;
  border: 3px solid white;
  height: 15px;
  width: 15px;
  cursor: pointer;
}
.repo__action.add {
  background: white;
}
.repo__action.delete {
  background: #0366d6;
}
</style>
