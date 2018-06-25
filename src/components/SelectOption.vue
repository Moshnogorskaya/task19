<template>
  <div class='select__group'>
      <select class='select-group__select'>
        <option disabled selected>Type</option>
        <option>Js</option>
      </select>
    <div class='select-group__arrow'>▼</div>
  </div>
</template>

<script>
export default {
  name: 'select-option',
  components: {},
};
</script>

<style>
.select__group {
  width: 20%;
  position: relative;
  height: 30px;
}

.select__group.warning {
  background: #fce6f1;
}

.select-group__select {
  z-index: 2;
  background: transparent;
  width: 100%;
  border-bottom: 1px solid #0366d6;
  font-size: 12px;
  appearance: none;
}

.select-group__arrow {
  position: absolute;
  z-index: 1;
  height: 100%;
  width: 20%;
  top: 0;
  right: 0;
  font-size: 1.2vmin;
  align-items: center;
  justify-content: center;
}

.select-group__select:focus {
  border-bottom: 2px solid #0366d6;
  outline: 0;
  box-shadow: none;
}
</style>
