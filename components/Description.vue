<template>
  <div id="description" class="description section">
    <h1 class="desc-title">
      John
      Piano & Voice Studio
    </h1>

    <div class="learn-more text-center">
      <a href="#" v-scroll-to="'#expertise'" class="scroll-promt">
        Learn more about what I do<br>
      </a>
      <a href="#" v-scroll-to="'#expertise'" class="dis-txt p-3 fas fa-arrow-down bounce h4"></a>
    </div>
  </div>
</template>

<script>
  export default {
    computed: {
      typedTxt() {
        return ['websites', 'applications', 'user interfaces'];
      }
    }
  };
</script>

<style lang="scss">
  @import '../assets/styles';

  .description {
    position: relative;
    display: flex;
    justify-content: center;
    flex-direction: column;
    height: 100vh; // because .section uns  ets height for mobile

    .learn-more {
      position: absolute;
      bottom: 75px;
      width: 100%;
    }

    .fas {
      color: $text_link;
    }

    .scroll-promt {
      display: none;
    }

  }

  @include breakpoint($breakpoint_screen_sm) {
    .description {
      text-align: center;

      .desc-title {
        margin: 0 $space_2;
      }

      .scroll-promt {
        display: inline;
      }
    }
  }
</style>
