
// this is where I create the bar over the jumbotron whit all the contacs

<template>
  <div class="mds-contact">
    <div class="container d-flex justify-content-between">
      <div>
        <i class="fas fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00
      </div>
      <div class="d-flex justify-content-around" v-for="(item, index) in contactsData" :key="index">
        <div class="mds-number px-2"><i :class="item.phone.logo"></i> {{item.phone.content}}</div>
        <div class="mds-mail px-2"><i :class="item.mail.logo"></i> {{item.mail.content}}</div>
        <div class="mds-social px-2"><i :class="item.facebook.logo"></i></div>
        <div class="mds-social px-2"><i :class="item.twitter.logo"></i></div>
        <div class="mds-social px-2"><i :class="item.linkedin.logo"></i></div>
      </div>
    </div>
  </div>
</template>

<script>
import contactsData from '../assets/data/contatcs.js';

export default {
  name: "Contacts",
  data(){
    return{
      contactsData
    }
  }
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
