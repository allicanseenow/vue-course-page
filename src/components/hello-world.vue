<template>
  <div class="root-container">
    <Navbar />
    <Contents />
  </div>
</template>

<script>
import { Navbar } from './navbar';
import { Contents } from './content';

export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  components: {
    Navbar,
    Contents,
  },
};
</script>

<style scoped>
.root-container {
  width: 100%;
  height: 100%;
  /* CSS Smooth Scroll */
  overflow-y: scroll;
  scroll-behavior: smooth;
  scroll-snap-type: y mandatory;
}
</style>
