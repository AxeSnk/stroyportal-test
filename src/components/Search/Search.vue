<template>
  <form class="search">
    <input
      type="text"
      class="search__input"
      placeholder="Хочу найти..."
      autocomplete="off"
      v-model="name"
      @focus="modal = true"
      v-click-outside="onClickOutside"
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
export default {
  data: function() {
    return {
      name: '',
      modal: false,
      names: ['Alexander', 'Fiona', 'Marina', 'Shrek'],
      filteredNames: [],
    };
  },
  mounted() {
    this.filterNames();
  },
  methods: {
    filterNames() {
      if(this.name.length == 0) {
        this.filteredNames = this.names
      }

      this.filteredNames = this.names.filter((name) => {
        return name.toLowerCase().startsWith(this.name.toLowerCase());
      });
    },
    setName(name) {
      this.name = name;
      this.modal = false;
    },
    onClickOutside(event) {
      const isItem = event.changedTouches[0].target.classList[0] == 'search__item'
      isItem ? null: this.modal = false;
    }
  },
  watch: {
    name() {
      this.filterNames();
    }
  }
};
</script>

<style lang="scss">
@import 'Search';
</style>
