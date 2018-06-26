<template>
<ul class="results-dashboard">
        <li class="results-dashboard__item">
          <dashboard-view />
        </li>
         <li class="results-dashboard__item">
          <dashboard-view />
        </li>
         <li class="results-dashboard__item">
          <dashboard-view />
        </li>
         <li class="results-dashboard__item">
          <dashboard-view />
        </li>
         <li class="results-dashboard__item">
          <dashboard-view />
        </li>
    </ul>
</template>

<script>
import DashboardView from './DashboardView.vue';

export default {
  name: 'results-dashboard',
  components: {
    DashboardView,
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
</style>
