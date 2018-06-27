<template>
  <div
  class="search__search-panel">
    <select-option :placeholder="'Type'" :options='types' />
    <select-option :placeholder='"Language"' :options='languages' />
    <input-keyword />
    <submit v-on:startSearch='composeURL'/>
  </div>
</template>

<script>
import SelectOption from './SelectOption.vue';
import InputKeyword from './InputKeyword.vue';
import Submit from './Submit.vue';
import types from '../utility/types';
import languages from '../utility/languages';

export default {
  name: 'search-panel',
  components: {
    SelectOption,
    InputKeyword,
    Submit,
  },
  data() {
    return {
      types,
      languages,
    };
  },
  methods: {
    composeURL() {
      console.log('url');
    },
  },
};
</script>

<style>
.search__search-panel {
  width: 100%;
  height: 60px;
  justify-content: space-between;
  align-items: flex-end;
  font-size: 16px;
}
</style>
