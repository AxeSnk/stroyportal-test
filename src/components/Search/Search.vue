<template>
  <form class="search">
    <input
      type="text"
      class="search__input"
      placeholder="Хочу найти..."
      autocomplete="off"
      v-model="name"
      @focus="modal = true"
      v-click-outside="hide"
    />
    <div class="search__list" v-if="filteredNames && modal">
      <ul>
        <li
          class="search__item"
          v-for="filteredName in filteredNames"
          v-bind:key="filteredName"
          @click="setName(filteredName)"
        >
          {{ filteredName }}
        </li>
      </ul>
    </div>
    <span class="search__icon"></span>
  </form>
</template>

<script>
import ClickOutside from "vue-click-outside";

export default {
  data: function () {
    return {
      name: "",
      modal: false,
      names: ["Alexander", "Fiona", "Marina", "Shrek"],
      filteredNames: [],
    };
  },
  mounted() {
    this.filterNames();
  },
  directives: {
    ClickOutside,
  },
  methods: {
    filterNames() {
      if (this.name.length == 0) {
        this.filteredNames = this.names;
      }

      this.filteredNames = this.names.filter((name) => {
        return name.toLowerCase().startsWith(this.name.toLowerCase());
      });
    },
    setName(name) {
      this.name = name;
      this.modal = false;
    },
    hide() {
      this.modal = false;
    },
  },
  watch: {
    name() {
      this.filterNames();
    },
  },
};
</script>

<style lang="scss">
@import "Search";
</style>
