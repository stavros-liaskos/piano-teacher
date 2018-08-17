<template>
  <div>
    <description/>
    <expertise/>
  </div>
</template>

<script>
  import Description from '~/components/Description.vue';
  import Expertise from '~/components/Expertise.vue';

  export default {
    components: {
      Description,
      Expertise
    }
  };
</script>
