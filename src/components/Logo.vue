<template>
  <div>
    <span>N E X </span>G E N
  </div>
</template>

<script>
export default {
  name: "Logo",
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
 
div{

  color: white;
  font-weight: 600;

  span{
    background-color: $bg-logo;
    color: $text-logo;
    padding: 8px 0 8px 25px;
    border-radius:25px 0 0 25px;
  }
}


</style>