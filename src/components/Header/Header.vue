<template>
  <header class="header">
    <div class="header__bar">
      <Bar />
    </div>
    <div class="header__main">
      <Section />
    </div>
  </header>
</template>

<script>
import Bar from '../Bar/Bar';
import Section from '../Section/Section';

export default {
  name: 'Header',
  components: {
    Bar,
    Section
  },
};
</script>

<style lang="scss">
@import 'Header';

</style>
