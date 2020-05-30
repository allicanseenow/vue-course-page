<template>
  <button>
    <slot />
  </button>
</template>

<script>
export default {
  name: 'Button',
};
</script>

<style lang="scss" scoped>
@import '../../styles/_variables.scss';

button {
  background-color: $primary-blue;
  color: $white;
  font-weight: 600;
  box-sizing: border-box;
  position: relative;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  cursor: pointer;
  outline: none;
  border: none;
  -webkit-tap-highlight-color: transparent;
  display: inline-block;
  white-space: nowrap;
  text-decoration: none;
  vertical-align: baseline;
  text-align: center;
  margin: 0;
  min-width: 64px;
  line-height: 36px;
  padding: 0 16px;
  border-radius: 4px;
  overflow: visible;
}
</style>
