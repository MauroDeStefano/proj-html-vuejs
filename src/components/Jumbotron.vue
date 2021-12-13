<template>
  <div class="mds-jumbotron">
    <div class="mds-darker-bg">
      <div class="mds-nav container d-flex justify-content-between">
        <div class="logo"><Logo /></div>
        <div class="mds-menu text-white ">
          <a class="px-3" v-for="(item, index) in navBtn" 
          :key="index">{{item.name}}</a>
          <i class="far fa-user px-3"></i>
          <a class="btn btn-info mds-btn ">GET IN TOUCH</a>
        </div>
      </div>
      <div class="container mt-5">
        <div class="row pt-5">
          <div class="col-4">
            <p class="mds-text-title">LOGISTICS SERVICES</p>
            <h1 class="mds-title-jumb text-white">CARGO <br>TRANSPORT</h1>
            <p class="mds-jumbo-text">Fractional or exclusive road cargo transportation to all regions, qhit small, medium and large vehicles.</p>
            <div>
              <a class="btn btn-info mds-btn ">GET IN TOUCH</a><a class="btn mds-btn-empty mx-3">READ MORE</a>
            </div>
          </div>
          <div class="col-4"></div>
          <div class="col-4"></div>
        </div>
      </div> 
    </div>
  </div>
</template>

<script>
import navBtn from '../assets/data/navBtn.js';
import Logo from './Logo.vue';

export default {
  name: "Jumbotron",
  data(){
    return{
      navBtn,
    }
  },
  components:{
    Logo,
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
 
.mds-jumbotron{
  
  background-image: url("../assets/img/bg-9.jpg");
  width: 100%;
  height: 600px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
 

  .mds-darker-bg{
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, .4);

    .mds-nav{
      height: 60px;
      line-height: 60px;

      a{
        text-decoration: none;
        color: white;
        font-weight: 600;
        font-size: 14px;
      }

      i{
        padding: 20px !important;
      }

    }

    .mds-title-jumb{
      font-size: 50px;
      font-weight: 900;
    }
  }
  
}
</style>