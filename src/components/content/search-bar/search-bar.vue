<template>
  <div class="searchbar-container">
    <div class="searchbar">
      <icon class="search_icon"><i class="fas fa-search"></i></icon>
      <input
        class="search_input"
        type="text"
        name=""
        placeholder="Search courses"
      />
    </div>
    <div class="search-stats"><b>23</b> of 98 courses match your search</div>
    <div class="search-functionality">
      <div class="sort-by">
        <i class="sort-icon fa fa-sort-amount-down"></i>
        <div class="sort-text">Sort by</div>
      </div>
      <div class="date-enrolled">
        <Button>
          <div class="button">
            <div class="text">Date enrolled</div>
            <i class="fas fa-chevron-down"></i>
          </div>
        </Button>
      </div>
    </div>
  </div>
</template>

<script>
import { Button } from '../../shared';
export default {
  name: 'SearchBar',
  components: { Button },
};
</script>

<style scoped lang="scss" src="./search-bar.scss"></style>
