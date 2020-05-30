<template>
  <div class="progress-bar-container">
    <div class="progress-bar" />
  </div>
</template>

<script>
export default {
  name: 'ProgressBar',
};
</script>

<style scoped lang="scss">
@import '../../styles/variables';

.progress-bar-container {
  background-color: #eeeeee;
  height: 6px;
  overflow: hidden;
  position: relative;

  div {
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
