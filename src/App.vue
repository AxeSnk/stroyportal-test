<template>
  <div class="wrapper">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header/Header';

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
  font-size: 14px;
  user-select: none;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
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

button {
  padding: 0;
  border-style: none;
}

input {
  border: none;
  padding: 0;
  outline: none;
}
</style>
