<template>
  <div class="navbar-container">
    <div class="navbar-inner-container">
      <h3 class="navbar-header">Your Courses</h3>
      <nav class="navbar">
        <ul>
          <li class="active">
            <a href="#home">To Do <mark>24</mark></a>
          </li>
          <li>
            <a href="#about">In Progress <mark>8</mark></a>
          </li>
          <li>
            <a href="#service">Completed<mark>5</mark></a>
          </li>
          <li>
            <a href="#contact">All Courses<mark>89</mark></a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style lang="scss" scoped>
@import './navbar.scss';
</style>
