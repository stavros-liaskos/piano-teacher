<template>
  <div class="section about">
    <headline-animated
      v-bind:class="['title m-b-3 text-center']"
      v-bind:content="'Piano and Voice Lessons'"/>

    <h4>30 minute lessons</h4>

    <br>
    <ul>
      <li>Pay Monthly: ($20 per week)</li>
      <li> Pay Quarterly: (Jan. - Mar 16, Mar. 16 - May 31st) ($19 per week)</li>
      <li>Pay Semesterly: (Jan - May) ($18 per week)</li>
    </ul>

    <br>
    <h4>45 minute lessons</h4>

    <br>
    <ul>
      <li>Pay Monthly: ($20 per week)</li>
      <li> Pay Quarterly: (Jan. - Mar 16, Mar. 16 - May 31st) ($19 per week)</li>
      <li>Pay Semesterly: (Jan - May) ($18 per week)</li>
    </ul>

    <br>
    <h4>60 minute lessons</h4>

    <br>
    <ul>
      <li>Pay Monthly: ($20 per week)</li>
      <li> Pay Quarterly: (Jan. - Mar 16, Mar. 16 - May 31st) ($19 per week)</li>
      <li>Pay Semesterly: (Jan - May) ($18 per week)</li>
    </ul>


    <br>
    <p>**I do not offer weekly plans </p>

    <p>Let's have a chat
      <a href="mailto:hello@stavrosliaskos.com" target="_blank">
        hello@stavrosliaskos.com
      </a> .
    </p>

    <go-home v-bind:style="{textAlign: 'right'}"/>
  </div>
</template>

<script>
  import HeadlineAnimated from '~/components/HeadlineAnimated';
  import GoHome from '~/components/GoHome';

  export default {
    components: {
      HeadlineAnimated,
      GoHome
    }
  };
</script>
