<template>
  <nav class="nav">
    <ul class="nav__list">
      <li v-for="item in list" :key="item.title" class="nav__item">
        <a class="nav__item-link" :href="item.href">{{item.title}}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data: () => ({
    list: [
      { title: 'Тендеры', href: '/mock-address/change-me' },
      { title: 'База подрядчиков', href: '/mock-address/change-me' },
      { title: 'Другие сервисы', href: '/mock-address/change-me' }
    ],
  }),
};
</script>

<style lang="scss">
@import 'Nav';
</style>
