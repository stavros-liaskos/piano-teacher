<template>
  <div class="app"
       v-bind:class="{ active: isNavOpen}"
  >
    <navigation/>

    <div class="container sidebar">
      <nuxt/>
    </div>

    <footer-bar/>

    <!--
        <header-bar/>
    -->

    <particles/>
  </div>
</template>

<script>
  import Navigation from '~/components/Navigation.vue';
  import Particles from '~/components/Particles.vue';
  import FooterBar from '~/components/Footer/FooterBar.vue';
  // import HeaderBar from '~/components/HeaderBar.vue';
  import FontFaceObserver from 'fontfaceobserver';

  export default {
    components: {
      Navigation,
      Particles,
      // HeaderBar,
      FooterBar
    },

    data() {
      return {
        isNavOpen: false
      };
    },

    methods: {
      /**
       * Initialize Navigation Listener for toggling state of Burger, Navigation, app elements
       */
      initNavigationListener() {
        this.$root.$on('toggle.navigation.state', (isNaviOpen) => {
          this.isNavOpen = !isNaviOpen;
        });
      },

      fontFaceLoader() {
        // Font loading: https://github.com/zeit/next.js/issues/512
        const robotoUrl = 'https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300',
          fontAwesomeUrl = 'https://use.fontawesome.com/releases/v5.0.6/css/all.css';

        let linkRoboto = document.createElement('link'),
          linkFontAwesome = document.createElement('link'),
          roboto = new FontFaceObserver('Roboto'),
          fontAwesome = new FontFaceObserver('FontAwesome');

        linkRoboto.href = robotoUrl;
        linkRoboto.rel = 'stylesheet';
        linkFontAwesome.href = fontAwesomeUrl;
        linkFontAwesome.rel = 'stylesheet';

        document.head.appendChild(linkRoboto);
        document.head.appendChild(linkFontAwesome);

        // roboto.load().then(() => {
        Promise.all([roboto.load(), fontAwesome.load()]).then(function () {
          document.documentElement.classList.add('roboto');
        }, function () {
          console.log('🍺');
        });
      }
    },

    mounted() {
      this.initNavigationListener();
      this.fontFaceLoader();
    }
  };
</script>

<style lang="scss" scoped>
  @import '../assets/styles';

  .app {
    width: 100%;
    font-family: $font_family_default !important;

    .container {
      min-height: calc(100vh - #{$footer_height});
    }

    // aside space
    .sidebar {
      padding: 0 $space_4;
    }
  }

  @include breakpoint($breakpoint_screen_md) {
    .app {
      .sidebar {
        margin: 0 0 0 $navi_toolbar_desktop_width;
        padding: 0 $space_5;
      }
    }
  }

  @include breakpoint($screen_viewport_lg) {
    .app {
      .sidebar {
        padding: 0 $space_7;
      }
    }
  }

  @include breakpoint($screen_viewport_xl) {
    .app {
      .sidebar {
        padding: 0 $space_9;
      }
    }
  }
</style>
