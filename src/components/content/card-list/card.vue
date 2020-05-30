<template>
  <div class="card-container">
    <div class="card-image" />
    <ProgressBar />
    <div class="card-content">
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
      <div class="button-container">
        <Button lightColor>View Progress</Button>
        <Button>Resume</Button>
      </div>
    </div>
  </div>
</template>

<script>
import { Button, ProgressBar } from '../../shared';
export default {
  name: 'Card',
  props: {
    title: String,
    text: Object,
  },
  components: { Button, ProgressBar },
};
</script>

<style scoped src="./card.scss" lang="scss"></style>
