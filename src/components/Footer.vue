<template>
  <div>
    <FootMenu />
    <Credits />
  </div>
</template>

<script>

import FootMenu from './FootMenu.vue';
import Credits from './Credits.vue';


export default {
  name: "Footer",
  components:{
    FootMenu,
    Credits
  }

}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

</style>