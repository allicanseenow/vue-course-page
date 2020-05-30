<template>
  <div class="progress-bar-container">
    <div class="progress-bar" :style="{ transform: calculateRate }" />
  </div>
</template>

<script>
export default {
  name: 'ProgressBar',
  props: {
    percent: {
      type: Number,
      default: 0,
    },
  },
  computed: {
    calculateRate() {
      return `translateX(-${100 - this.percent}%)`;
    },
  },
};
</script>

<style scoped lang="scss">
@import '../../styles/variables';

.progress-bar-container {
  background-color: #eeeeee;
  height: 6px;
  overflow: hidden;
  position: relative;

  .progress-bar {
    transform: translateX(-25%);

    background-color: $cyan;
    transition: transform 0.4s linear;
    top: 0;
    left: 0;
    width: 100%;
    bottom: 0;
    position: absolute;
    transform-origin: left;
  }
}
</style>
