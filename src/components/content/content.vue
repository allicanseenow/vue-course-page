<template>
  <div class="container">
    <SearchBar />
    <CardList />
  </div>
</template>

<script>
import { SearchBar } from './search-bar';
import { CardList } from './card-list';

export default {
  name: 'Contents',
  components: {
    SearchBar,
    CardList,
  },
};
</script>

<style lang="scss" scoped src="./content.scss"></style>
