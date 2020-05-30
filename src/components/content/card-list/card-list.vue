<template>
  <div class="card-list-container">
    <Card
      img-src="https://images.unsplash.com/photo-1477346611705-65d1883cee1e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
      title="Brutalist Architecture"
      text="Learn the secrets of the hand model industry in this 4 part course. Here's some more text and some more"
    />
    <Card
      img-src="https://images.unsplash.com/photo-1485470733090-0aae1788d5af?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1091&q=80"
      :completionRate="100"
      title="Surfing Safety"
      text="Stay safe while getting barreled this summer. We'll look at wave etiqute, how to rock-off safely and how to properly secure your umbrella"
    />
    <Card
      img-src="https://images.unsplash.com/photo-1495546992359-94a48035efca?ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"
      :completionRate="60"
      title="Delicious berries"
      text="Everyone loves berries, so let's learn about strawberries, raspberries"
    />
    <Card
      img-src="https://images.unsplash.com/photo-1519380746410-8d9e2b5835d0?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
      :completionRate="40"
      title="Delicious berries"
      text="Everyone loves berries, so let's learn about strawberries, raspberries"
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
  display: flex;
  flex-wrap: wrap;
  margin: 3.5rem -15px;

  div {
    margin: 0 15px 2rem;
  }
}
</style>
