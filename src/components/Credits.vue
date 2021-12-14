<template>
  <div class="credits">
    <div class="mds-text-wide-s container d-flex justify-content-between align-content-center mds-text-gray">
    <div>Enjoy the low price. are tracking any intention of piracy</div>
    <div><i class="far fa-copyright"></i>2021 NEXGEN is Proudly Powered by <a href="https://github.com/MauroDeStefano" target="_blanck">Mauro De Stefano</a>.</div>
    </div>
    <a href="#"><i class="mds-return-up fas fa-arrow-up"></i></a>
  </div>
</template>

<script>
export default {
  name: "Credits",
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

.credits{
  position: relative;
  width: 100%;
  height: 50px;
  background-color: #0D0D11;
  line-height: 50px;

  a{
    text-decoration: none;
    color: #0A5662;
  }

  .mds-return-up{
    position: absolute;
    top: 50%;
    right: 10px;
    transform: translateY(-50%);
    padding: 10px;
    background-color: #29292D;
    color:#101D21;
    border-radius: 50%;
  }
}
</style>