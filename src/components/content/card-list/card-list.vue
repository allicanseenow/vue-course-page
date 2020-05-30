<template>
  <div class="card-list-container">
    <Card
      title="Surfing Safety"
      text="Stay safe while getting barreled this summer. We'll look at wave etiqute, how to rock-off safely and how to properly secure your umbrella"
    />
  </div>
</template>

<script>
import Card from './card';

export default {
  name: 'CardList',
  components: { Card },
};
</script>

<style scoped lang="scss">
.card-list-container {
  margin-top: 3.5rem;
  margin-bottom: 3.5rem;
}
</style>
