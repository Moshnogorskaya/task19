<template>
<div class="repo-dashboard__stats">
      <div class="repo-dashboard__language">Language</div>
      <div class="repo-dashboard__stars stars">
        <span class="stars__icon">
          <i class="fas fa-star"></i>
        </span>
        100
      </div>
    </div>
</template>

<script>
export default {
  name: 'dashboard-view-stats',
  components: {
  },
};
</script>

<style>
.repo-dashboard__stats {
  height: 20%;
  justify-content: space-between;
}
.repo-dashboard__language {
  color: #999999;
  font-size: 12px;
  align-items: center;
}
.repo-dashboard__stars {
  font-size: 18px;
  align-items: center;
}

.stars__icon {
  color: #f1e05a;
  margin-right: 6px;
  font-size: 18px;
  position: relative;
  top: -2px;
}
</style>
