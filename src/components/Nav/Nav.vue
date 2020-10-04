<template>
  <nav class="nav">
    <div
      class="nav__burger"
      @click="toggleNav()"
      v-click-outside="hideNav"
    ></div>
    <ul class="nav__list" v-bind:class="{ nav__list_active: active }">
      <li v-for="item in list" :key="item.title" class="nav__item">
        <a class="nav__item-link" :href="item.href">{{ item.title }}</a>
        <span v-if="item.expanded" class="nav__item-arrow"></span>
      </li>
    </ul>
  </nav>
</template>

<script>
import ClickOutside from 'vue-click-outside';

export default {
  data: () => ({
    list: [
      { title: 'Тендеры', href: '/mock-address/change-me' },
      { title: 'База подрядчиков', href: '/mock-address/change-me' },
      {
        title: 'Другие сервисы',
        href: '/mock-address/change-me',
        expanded: true,
      },
    ],
    active: false,
  }),
  directives: {
    ClickOutside,
  },
  methods: {
    toggleNav() {
      this.active = !this.active;
    },
    hideNav() {
      this.active = false
    }
  },
};
</script>

<style lang="scss">
@import 'Nav';
</style>
