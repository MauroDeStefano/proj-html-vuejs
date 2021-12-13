<template>
  <div class="container">
    <div class="row mt-5">
      <div class="mt-5 col-8">
        <p class="text-emp">WHO WE ARE</p>
        <h2><span class="text-emp bg-text-emp"><i class="far fa-gem"></i> Excellence </span>  in Transport</h2>
      </div>
      <div class="mt-5 col-4">
        <p class="fw-bold">Vehicle Types</p>
        <div class="row mds-truck-type" v-for="(item, index) in truckWeigth" :key="index">
          <div class="col-4">
            <img class="w-100 mds-img-type" :src="item.image" :alt="item.name">
          </div>
          <div class="col-8">
            <h5 class="fw-bold">{{item.name}}</h5>
            <p class="mds-text-gray">Max Weight {{item.maxWeight}} Kg</p>
          </div>
        </div>
      </div>
      
    </div>
  </div>  
</template>

<script>

import truckWeigth from '../assets/data/truckWeight.js';

export default {
  name: "Prensentation",
  data(){
    return{
      truckWeigth,
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.container{
  .col-8{
    
    p{
      font-size: 10px;
      font-weight: 600;
    }

    h2{
    font-weight: 900;

      span{
        padding: 0 0 0 10px;
        margin-right: 5px ;
      }
    }
  }
  
  .col-4{
  
    .mds-img-type{
      padding: 5px;
      background-color: #DAECED;
    }
    .mds-truck-type{
      border-bottom: 2px solid rgba($color: gray, $alpha: .3);
    }
  }
  
}


</style>