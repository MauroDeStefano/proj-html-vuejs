<template>
  <div>
    <Presentation />
    <MainServices />
    <LogisticalProcedure />
    <Results />
  </div>
</template>

<script>
import Presentation from './Prensentation.vue';
import MainServices from './MainServices.vue';
import LogisticalProcedure from './LogisticalProcedure.vue';
import Results from './Results.vue';

export default {
  name: "Main",
  components:{
    Presentation,
    MainServices,
    LogisticalProcedure,
    Results
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

</style>