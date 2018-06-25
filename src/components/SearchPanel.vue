<template>
  <div class="search__search-panel">
    <select-option />
    <select-option />
    <input-keyword />
    <submit />
  </div>
</template>

<script>
import SelectOption from '@/components/SelectOption.vue';
import InputKeyword from '@/components/InputKeyword.vue';
import Submit from '@/components/Submit.vue';

export default {
  name: 'search-panel',
  components: {
    SelectOption,
    InputKeyword,
    Submit,
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

/* <Select
          options={types}
          required
          isValid={this.state.isValid}
          onChangeValue={this.handleTypeChange}
        />
        <Select
          options={languages}
          placeholder="Language"
          onChangeValue={this.handleLanguageChange}
        />
        <InputKeywords onChangeValue={this.handleKeywordChange} />
        <Submit
          onButtonClick={this.handleButtonClick}
          disabled={this.props.waiting}
        /> */
</style>
