<template>
  <div class="bar">
    <div class="bar__region">bar__region</div>
    <div class="bar__nav">
      <Nav />
    </div>
  </div>
</template>

<script>
import Nav from '../Nav/Nav';

export default {
  components: { Nav },
};
</script>

<style lang="scss">
@import 'Bar';
</style>
