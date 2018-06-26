<template>
  <div class='input'>
        <p
          :class="['input__placeholder', { input__placeholder_active: !active === false}]"
          class='input__placeholder'>
          Type here for search
        </p>
        <input
          :value="keyword"
          @input="$emit('input', $event.target.value)"
          @focus="active = true"
          @blur='active = false'
          type='text'
          maxLength='50'
          class='input__field'
        />
      </div>
</template>

<script>
export default {
  name: 'input-keyword',
  components: {},
  props: ['keyword'],
  data() {
    return {
      active: false,
    };
  },
};
</script>

<style>
.input {
  flex-direction: column;
  height: 50px;
  width: 35%;
  justify-content: space-between;
}

.input__placeholder {
  font-size: 12px;
  font-weight: normal;
  position: relative;
  top: 30px;
  z-index: 1;
}

.input__placeholder_active {
  font-size: 12px;
  color: #0366d6;
  top: 10px;
}

.input__field {
  font-size: 12px;
  height: 30px;
  border-bottom: 1px solid #0366d6;
  background: transparent;
  z-index: 2;
}

.input__field:focus {
  border-bottom: 2px solid #0366d6;
  outline: 0;
  box-shadow: none;
}
</style>
