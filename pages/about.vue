<template>
  <div class="section about">
    <headline-animated
      v-bind:class="['title m-b-3 text-center']"
      v-bind:content="'About me'"/>

    <h4>John's Piano Journey</h4>

    <br>
    <p>John is a classical pianist and accompanist, vocalist, singer/songwriter and piano teacher. With 4 years
      of teaching experience, John has taught a range of students from elementary beginners to experienced college
      students. She has studied piano for 16 years with master teachers nationwide, including Dr. Gary Wolf, a past
      professor at Rollins College. She has studied Master's level vocal studies from Dr. Mindy Damon, a current Liberty
      University professor and previous Disney's Epcot: Voices of Liberty performer. John is currently teaching piano
      in Orlando, Florida and singing professionally with Central Florida Community of the Art's ensemble called
      Legacy!.
    </p>
    <p>Throughout her life, John has had a passion for the arts. Whether it be music, dance, acting, etc. she finds
      meaning in each form and is passionate about the impact the arts has on the community. She has been a yearly
      participant and winner of the Florida Federation of Music, National Music Guild Association, and has performed
      charity concerts for the community. She attended Douglas Anderson School of the Arts for high school and was
      featured in their Extravaganza! performances as a solo pianist. </p>

    <p>John finds joy and fulfillment through her impact on the community - especially in teaching. Through her faith
      and heart for people, she is pursuing her goals in the arts as a musician, actress, and teacher. Her most recent
      acting work was filming a short for Jesus Films - Campus Crusade for Christ and Disney World!
    </p>

    <p>John is excited to hear from you for your first piano lesson and you can sign up on her mailing list or contact
      her on the Contact page. </p>

    <p>Have an amazing and magical day!</p>

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
