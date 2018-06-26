<template>
 <div class="view">
        <button
          class='view__dashboard'>
          <i class="fas fa-th-large"></i>
        </button>
        <button class='view__list'>
         <i class="fas fa-bars"></i>
        </button>
      </div>
</template>

<script>

export default {
  name: 'toggle-view',
  components: {
  },
};
</script>

<style>

.view {
  width: 100%;
  height: 77px;
  justify-content: flex-end;
}

.view__dashboard {
  width: 40px;
  justify-content: flex-end;
  align-items: center;
  cursor: pointer;
  margin-right: 10px;
  font-size: 32px;
  color: #e0e0e0;
}

.view__list {
  width: 40px;
  justify-content: flex-end;
  align-items: center;
  cursor: pointer;
  font-size: 36px;
  color: #e0e0e0;
}

.view__dashboard.active,
.view__list.active {
  color: #3c4146;
}

.view__dashboard:focus,
.view__list:focus {
  outline: none;
  border: none;
  box-shadow: none;
}

</style>
