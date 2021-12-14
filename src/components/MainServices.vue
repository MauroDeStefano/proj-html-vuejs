<template>
  <div class="mds-service-section">
    <div class="container">
      <p class="text-emp mds-text-wide-s">ROAD TRANSPORT</p>
      <h2 class="mb-3 text-white mds-title-wide">Main <span class="text-emp bg-text-emp text-white rounded">Services</span></h2>
      <div class="d-flex justify-content-between mt-2 mb-5">
        <p class=" text-white w-75 ">With all of this expertise anda capability comes an unrivalled commitment to customer service. We will work hard to understand your needs in order to develop a productive, long-term partnership.</p>
        
        <a class=" btn mds-btn-empty mds-btn-service fw-bold" href="">SEE ALL</a>
      </div>
      <div class="row">
        <div v-for="(item,index) in mainServicesData" :key="index" class="col mds-services-card mx-3">
          <i :class="item.fontAwsome" class="mds-main-i"></i>
          <h5 class="fw-bolder">{{item.name}}</h5>
          <p>{{item.description}}</p>
          <i class="fas fa-arrow-right"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import mainServicesData from '../assets/data/mainServicesData.js';


export default {
  name: "MainServices",
  data(){
    return{
      mainServicesData
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.mds-service-section{
  background-color: #111117;
  width: 100%;
  margin-top: 100px;
  padding: 100px 0;

  .container{

    h2{
      
      span{
        padding: 0 7px;
        margin: 0 2px;
      } 
    }

    .mds-btn-service{
      height: 40px;
      width: 100px;
    }

    .mds-services-card{
      position: relative;
      background-color: #19191F;
      padding: 30px;
      border-radius: 5px;
      color: white;

      i{
        color: #058283;
      }

      .mds-main-i{
        font-size: 35px;
        padding: 15px;
        border-radius: 50%;
        background-color: #16282E;
        margin-bottom: 15px;
      }

      .fa-arrow-right{
        font-size: 25px;
        position: absolute;
        top: 30px;
        right: 30px;
      }

    }

  }
}
</style>