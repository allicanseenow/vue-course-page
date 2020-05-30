<template>
  <div class="container">
    <SearchBar />
  </div>
</template>

<script>
import SearchBar from './search-bar';

export default {
  name: 'Contents',
  components: {
    SearchBar,
  },
};
</script>

<style lang="scss" scoped src="./content.scss"></style>
