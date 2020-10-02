<template>
  <div class="bar">
    <div class="bar__region">
      <Geo />
    </div>
    <div class="bar__nav">
      <Nav />
    </div>
  </div>
</template>

<script>
import Nav from "../Nav/Nav";
import Geo from "../Geo/Geo";

export default {
  data: () => ({
    coordinates: {
      lat: 0,
      lng: 0
    }
  }),
  created() {

  },
  components: { Nav, Geo },
};
</script>

<style lang="scss">
@import "Bar";
</style>
