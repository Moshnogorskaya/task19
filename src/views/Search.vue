<template>
  <div class="search">
    <search-panel @submitSearch='getRepos' />
    <results v-if='Object.keys(repos).length' :repos='repos' />
    <no-results v-else />
  </div>
</template>

<script>
import SearchPanel from '@/components/searchPanel/SearchPanel.vue';
import Results from '@/components/Results.vue';
import NoResults from '@/components/NoResults.vue';
import getGithubData from '@/components/utility/get-github-data';
import prepareDataToDisplay from '@/components/utility/prepare-data-to-display';

export default {
  name: 'search',
  components: {
    SearchPanel,
    Results,
    NoResults,
  },
  data() {
    return {
      repos: {},
    };
  },
  methods: {
    getRepos(url) {
      console.log('search is started');
      getGithubData(url).then((response) => {
        console.log(response.data.items);
        const myRepos = prepareDataToDisplay(response.data.items);
        console.log(myRepos);
        this.repos = myRepos;
      });
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
