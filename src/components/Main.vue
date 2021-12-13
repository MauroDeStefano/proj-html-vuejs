<template>
  <div>
    <Presentation />
    <MainServices />
    <LogisticalProcedure />
  </div>
</template>

<script>
import Presentation from './Prensentation.vue';
import MainServices from './MainServices.vue';
import LogisticalProcedure from './LogisticalProcedure.vue';

export default {
  name: "Main",
  components:{
    Presentation,
    MainServices,
    LogisticalProcedure
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

</style>