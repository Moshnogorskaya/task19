<template>
  <ul class="results-dashboard">
    <li v-for='(value, key) in repos' :key='key' class="results-dashboard__item">
      <div class="repo-dashboard">
        <dashboard-view-stats :repo='value' />
        <dashboard-view-info :repo='value' />
        <div class="button-wrapper">
          <button
            class='repo-dashboard__action delete'>REMOVE FROM LIST
          </button>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
import DashboardViewStats from './DashboardViewStats.vue';
import DashboardViewInfo from './DashboardViewInfo.vue';

export default {
  name: 'results-dashboard',
  props: ['repos'],
  components: {
    DashboardViewStats,
    DashboardViewInfo,
  },
};
</script>

<style>
.results-dashboard {
  width: 93%;
  flex-wrap: wrap;
}
.results-dashboard__item {
width: 50%;
}
.repo-dashboard {
  width: 100%;
  height: 275px;
  flex-direction: column;
  border: 1px solid #e0e0e0;
  box-shadow: 0px 2px 3px rgba(0, 0, 0, 0.25);
  margin: 3%;
  padding: 3px 25px 0 40px;
}
.button-wrapper {
  height: 25%;
  align-items: flex-start;
  justify-content: center;
  padding-top: 1px;
}
.repo-dashboard__action {
  color: white;
  border: none;
  height: 55%;
  font-weight: 100;
  font-size: 12px;
  transition: background-color 0.5s;
  box-shadow: 0px 2px 3px rgba(0, 0, 0, 0.25);
  justify-content: center;
  cursor: pointer;
}
.repo-dashboard__action.add {
  background: #0366d6;
  width: 37%;
}
.repo-dashboard__action.delete {
  background: #eb5757;
  width: 50%;
}
.repo-dashboard__action:focus {
  outline: none;
}
.repo-dashboard__action:active {
  box-shadow: none;
}
</style>
