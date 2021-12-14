<template>
  <div>
    <Presentation />
    <MainServices />
    <Procedure />
    <Results />
    <TrustedFeedback />
    <GetInTouch />
  </div>
</template>

<script>
import Presentation from './Prensentation.vue';
import MainServices from './MainServices.vue';
import Procedure from './Procedure.vue';
import Results from './Results.vue';
import TrustedFeedback from './TrustedFeedback.vue';
import GetInTouch from './GetInTouch.vue';

export default {
  name: "Main",
  components:{
    Presentation,
    MainServices,
    Procedure,
    Results,
    TrustedFeedback,
    GetInTouch
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

</style>