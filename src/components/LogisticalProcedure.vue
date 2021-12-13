<template>
  <div class="my-5 text-center">
    <div class="container">
      <p class="text-emp mds-text-wide-s fw-bolder">HOW IT WORKS IN PRACTICE</p>
      <h2 class="mb-3 fw-bolder"><span class="text-emp bg-text-emp px-2 rounded">Logistical</span> Procedure</h2>
      <p class="mds-text-gray">We work with innovative methologies to ensure the the entire delivery process is done from start to finish as planned.</p>
    </div>
    <div class="mds-arificial-hr">
    <div class="row mds-this-row">
      <div class="col mds-logistical-card" v-for="(item, index) in logisticalData" :key="index"> 
        <div class="mds-logistical-number">0{{index + 1}}</div>
        <h5>{{item.name}}</h5>
        <p class="mds-text-gray">{{item.description}}</p>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
import logisticalData from '../assets/data/logisticalData.js'; 

export default {
  name: "logisticalProcedure",
  data(){
    return{
      logisticalData
    }
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';


.mds-arificial-hr{
  margin-top: 70px;
  width: 100%;
  height: 5px;
  background-color: #CBE3DE;
}

.mds-this-row{
  width: 99%;
  margin: 0 auto;
  min-width: 1000px;
}

.mds-logistical-card{
  margin-top: -15px!important;

  h5{
    color: #1E313E;
    font-weight: 700;
  }


}

.mds-logistical-number{
  width: 35px;
  height: 35px;
  margin: 0 auto;
  line-height: 35px;
  border-radius: 50%;
  background-color: #DAECED;
  margin-bottom: 20px;
  color: $text-logo;
  font-weight: 700;
}

</style>