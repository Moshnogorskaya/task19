<template>
  <div class="search">
    <search-panel @submitSearch='getRepos' />
    <results v-if='repos' :repos='repos' />
    <no-results v-else />
  </div>
</template>

<script>

import SearchPanel from '@/components/searchPanel/SearchPanel.vue';
import Results from '@/components/Results.vue';
import NoResults from '@/components/NoResults.vue';

const repo1 = {
  id: 100,
  name: 'Repo',
  description: 'description',
  language: 'languageeee',
  html_url: '',
  stargazers_count: 200,
  topics: ['topic', 'topic', 'topic'],
  saved: false,
};

const repo2 = {
  id: 200,
  name: 'Repo',
  description: 'description',
  language: 'languageeee',
  html_url: '',
  stargazers_count: 200,
  topics: ['topic', 'topic', 'topic'],
  saved: false,
};
const repo3 = {
  id: 300,
  name: 'Repo',
  description: 'description',
  language: 'languageeee',
  html_url: '',
  stargazers_count: 200,
  topics: ['topic', 'topic', 'topic'],
  saved: false,
};

const repos = {
  [repo1.id]: repo1,
  [repo2.id]: repo2,
  [repo3.id]: repo3,
};

export default {
  name: 'search',
  components: {
    SearchPanel,
    Results,
    NoResults,
  },
  data() {
    return {
      repos,
    };
  },
  methods: {
    getRepos() {
      console.log('search is started');
      console.log(this.repos[100]);
    },
  },
};
</script>

<style>
.search {
  flex-direction: column;
  align-items: center;
  width: 80%;
}

</style>
