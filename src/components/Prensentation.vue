<template>
  <div class="container mb-5">
    <div class="row mt-5 mb-5">

      <!-- Left part of the presentation section -->

      <div class="mt-5 col-8 mds-left-presentation">
        <p class="text-emp mds-text-wide-s">WHO WE ARE</p>
        <h2 class="mb-3"><span class="text-emp bg-text-emp rounded"><i class="far fa-gem"></i> Excellence </span>  in Transport</h2>
        <p class="mds-text-gray">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Doloremque voluptas vel et! Repudiandae, dolore placeat vero odit nihil minus voluptatum tenetur quibusdam numquam nam? Consequuntur ipsam assumenda perferendis voluptatum commodi!</p>
        <p class="mds-text-gray">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam corrupti architecto repellendus explicabo? Sint esse ad sunt cumque, sed corporis delectus quam ratione voluptates similique blanditiis veniam, distinctio error minima?</p>
        <p class="text-cit mds-text-gray ">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam corrupti ab non eius omnis culpa quidem rem quas pariatur molestias, placeat provident tempora officia numquam! Temporibus nisi ad voluptas aperiam.</p>
        <p class="mds-text-gray">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Provident saepe sed exercitationem.</p>
        <ul>
          <li class="mds-text-gray" v-for="(item, index) in highlights" :key="index">{{item.point}}</li>
        </ul>
      </div>




      <!-- Rigth part of the presentation sections -->

      <div class="mt-5 col-4 mds-right-presentation">
        <p class="fw-bold">Vehicle Types</p>

        <!-- a cycle that take all the kind of trucks -->
        <div class="row mds-truck-type" v-for="(item, index) in truckWeigth" :key="index">
          <div class="col-4">
            <img class="w-100 mds-img-type" :src="item.image" :alt="item.name">
          </div>
          <div class="col-8">
            <h5 class="fw-bold">{{item.name}}</h5>
            <p class="mds-text-gray">Max Weight {{item.maxWeight}} Kg</p>
          </div>
        </div>

        <!-- cycle to have all the certification we want to show -->
        <div>
          <p class="fw-bold">Certifications</p>
          <img class="mds-certificate" v-for="(item, index) in certifications" :key="index" :src="item.logo" :alt="item.name">
        </div>
      </div>
      
    </div>
  </div>  
</template>

<script>

import truckWeigth from '../assets/data/truckWeight.js'; 
import certifications from '../assets/data/certifications.js';
import highlights from '../assets/data/highlights.js';


export default {
  name: "Prensentation",
  data(){
    return{
      truckWeigth,
      certifications,
      highlights
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.container{
  .mds-left-presentation{

    p, li{
      font-size: 10px;
      font-weight: 600;
    }

    ul{
      padding: 10px;
      list-style: colo;
      list-style: none;
    }

    li::before {
      content: "\2022";
      color: gray;
      font-weight: bold;
      display: inline-block; 
      width: 1em;
      margin-left: -1em;
    }

    h2{
    font-weight: 900;

      span{
        padding: 0 0 0 10px;
        margin-right: 5px ;
      }
    }
  }
  
  .mds-right-presentation{
  
    .mds-img-type{
      padding: 5px;
      background-color: #DAECED;
    }
    .mds-truck-type{
      margin-bottom: 10px;
      border-bottom: 2px solid rgba($color: gray, $alpha: .3);
    }
    .mds-truck-type:last-child{
      border: none!important;
    }

    .mds-certificate{
      width: 120px;
      margin-right: 15px;
    }
  }
  
}


</style>