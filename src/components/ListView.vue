<template>
 <div class="repo">
        <div class="wrapper-repo-action">
          <button class='repo__action' />
        </div>
        <list-view-info />
        <list-view-stats />
      </div>
</template>

<script>

import ListViewInfo from '@/components/ListViewInfo.vue';
import ListViewStats from '@/components/ListViewStats.vue';

export default {
  name: 'list-view',
  components: {
    ListViewInfo,
    ListViewStats,
  },
};
</script>

<style>
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
