<template>
  <header class="header">
    <div class="header__bar">
      <Bar />
    </div>
  </header>
</template>

<script>
import Bar from '../Bar/Bar';

export default {
  name: 'Header',
  components: {
    Bar
  },
};
</script>

<style lang="scss">
@import 'Header';

</style>
