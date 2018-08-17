<template>
  <div class="expertise-card one-third bg-light">
    <img class="" v-lazy="`${img}`" v-bind:alt="[title]">
    <h2 class="h1">{{title}}</h2>
  </div>
</template>

<script>
  export default {
    props: {
      title: String,
      img: String
    }
  };
</script>

<style lang="scss" scoped>
  @import '../assets/styles';

  $expertise_icons_color: $text_link;

  .one-third {
    width: 100%;
  }

  .expertise-card {
    text-align: center;

    * {
      padding: $space_2;
    }

    .fas {
      font-size: $expertise_icons_size;
      color: $expertise_icons_color;
    }
  }

  @include breakpoint($breakpoint_screen_md) {
    .one-third {
      max-width: 33%;
    }
  }
</style>
