<template>
  <div class="mds-results">
    <div class="container text-center">
      <p class="text-emp mds-text-wide-s fw-bolder">WHAT ARE WE DOING</p>
      <h2 class="mb-3 fw-bolder text-white"><span class="text-emp bg-text-emp px-2 rounded text-white">Results</span> in Numbers</h2>
      <div class="row mt-5">
        <div v-for="(item,index) in resultData" :key="index" class="mds-result-card col p-5">
          <h3 class="text-emp fw-bolder">{{item.number}}</h3>
          <h5 class="text-white fw-bold m-3">{{item.name}}</h5>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import resultData from '../assets/data/resultsData.js';

export default {
  name: "Results",

  data(){
    return{
      resultData
    }
  }

}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.mds-results{
  padding: 100px 0 ;
  margin-top: 250px;
  background-image: url("../assets/img/bg-10.jpg") ;
  height: 500px;
  background-position: center;
}
</style>