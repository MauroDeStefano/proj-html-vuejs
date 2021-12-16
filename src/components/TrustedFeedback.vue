<template>
  <div class="trusted-feedback">
    <div class="container text-center">
      <p class="text-emp mds-text-wide-s">CUSTOMERS TESTIMONIALS</p>
       <h2 class="mb-3 text-white mds-title-wide">Trusted <span class="text-emp bg-text-emp text-white rounded px-2">Feedback</span></h2>
       <p class="mds-text-gray w-75 m-auto">
         We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for recognition.
       </p>

       <!-- Cycle of cards containing the feedbacks -->
       <div class="row mt-5">
         <div class="mds-card-trusted col text-start text-white" 
         v-for="(item, index) in trustedData" :key="index">
          <img class="mds-trusted-img" :src="item.logo" alt="item.name">
          <p class="mt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni, totam sed. Unde aut nulla maxime ipsam ratione labore laborum ducimus debitis, animi beatae at id explicabo! Nisi eveniet ipsam in?</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui error obcaecati nihil </p>
          <i class="fas fa-quote-right"></i>
         </div>
       </div>
    </div>
  </div>
</template>

<script>

import trustedData from '../assets/data/trustedData.js';

export default {
  name: "TrustedFeedback.vue",
  data(){
    return{
      trustedData,
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.trusted-feedback{
  background-color: #111117;
  padding: 100px 0 70px 0;
}

.mds-card-trusted{
  position: relative;
  padding: 30px 35px;
  background-color: $bg-cards;
  margin: 0 10px;
  font-size: 12px;

  i{
     position:absolute;
     color: #46464B;
     bottom: 30px;
     right: 30px;
     font-size: 25px;
  }
}

.mds-trusted-img{
  filter: brightness(600%);
  width: 50%;
}

</style>