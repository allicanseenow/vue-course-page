<template>
  <div class="card-container">
    <div class="card-image" :style="{ 'background-image': `url(${imgSrc})` }" />
    <ProgressBar :percent="completionRate" />
    <div class="card-content">
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
      <div class="button-container">
        <Button lightColor v-if="inProgress">View Progress</Button>
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
    text: String,
    completionRate: Number,
    imgSrc: String,
  },
  components: { Button, ProgressBar },
  computed: {
    inProgress() {
      if (!this.completionRate) return false;
      return this.completionRate > 0;
    },
  },
};
</script>

<style scoped src="./card.scss" lang="scss"></style>
