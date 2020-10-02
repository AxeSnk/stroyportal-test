<template>
  <div class="section">
    <div class="section__logo">
      <Logo />
    </div>
    <div class="section__catalog">
      <Catalog />
    </div>
    <div class="section__search">
      <Search />
    </div>
    <div class="section__list">
      <List />
    </div>
    <div class="section__login">
      <User />
    </div>
  </div>  
</template>

<script>
import Logo from '../Logo/Logo';
import Catalog from '../Catalog/Catalog';
import Search from '../Search/Search';
import List from '../List/List';
import User from '../User/User';

export default {
  components: {
    Logo,
    Catalog,
    Search,
    List,
    User
  }
};
</script>

<style lang="scss">
@import 'Section';
</style>
