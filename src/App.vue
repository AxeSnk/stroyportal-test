<template>
  <div class="wrapper">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header/Header'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
@import '@/assets/fonts/fonts.scss';
@import '@/assets/styles/styles.scss';

body {
  margin: 0;
}

.wrapper {
  font-family: "open-sans";
}

ul {
  margin-block-start: 0;
  margin-block-end: 0;
  padding-inline-start: 0;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
  color: $hint
}
</style>
