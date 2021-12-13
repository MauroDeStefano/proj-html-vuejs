
// this is where I create the bar over the jumbotron whit all the contacs

<template>
  <div class="mds-contact">
    <div class="container d-flex justify-content-between">
      <div>
        <i class="fas fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00
      </div>
      <div class="d-flex justify-content-around">
        <div class="mds-number px-2"><i class="fas fa-phone-alt"></i> +1(305) 1234-5678</div>
        <div class="mds-mail px-2"><i class="fas fa-envelope"></i> hello@example.com</div>
        <div class="mds-social px-2"><i class="fab fa-facebook-f"></i></div>
        <div class="mds-social px-2"><i class="fab fa-twitter"></i></div>
        <div class="mds-social px-2"><i class="fab fa-linkedin-in"></i></div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: "Contacts",
}
</script>

<style lang="scss" scoped>
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';


.mds-contact{
  background-color: $bg-contacts;
  height: 40px;
  width: 100%;
  color: $text-contacts;
  font-size: 12px;

  div{
    line-height: 40px;
    
  }
}

</style>>
