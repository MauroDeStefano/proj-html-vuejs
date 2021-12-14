<template>
  <div class="foot-menu">
    <div class="container">
      <div class="row">
        <div v-for="(item, index) in contacts" :key="index" class="col mds-text-gray mds-foot-contact">
          <Logo />
          <p class="my-4">
            A Functional HTML Template for Corporate & Business.
          </p>
          <p class="mb-1"><i :class="item.phone.logo"></i>{{item.phone.content}}</p>
          <p class="mb-1"><i :class="item.mail.logo"></i>{{item.mail.content}}</p>
          <p class="mb-4"><i :class="item.address.logo"></i>{{item.address.content}}</p>
          <a class="btn mds-btn-empty">GET IN TOUCH</a>
        </div>

        <div v-for="(menu) in menus" :key="menu.idKey" class="col mds-footer-card mds-text-gray">
          <h4 class="text-white mds-title-wide">{{menu.name}}</h4>
          <ul class="mds-foot-list">
            <li v-for="(item, index) in menu.contents" :key="index">
              <i class="fas fa-chevron-right"></i>{{item.name}}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from './Logo.vue';
import contacts from '../assets/data/contatcs.js';
import menus from '../assets/data/footMenuData.js'

export default {
  name: "FootMenu",
  components:{
    Logo
  },
  data(){
    return{
      contacts,
      menus
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';


.foot-menu{
  background-color: #111117;
  width: 100%;
  padding: 100px 0;
}

.mds-foot-contact i{
  margin-right: 10px;
}

.row{
  div{
    margin-right: 15px;
  }
}

.mds-footer-card{
  background-color: #19191F;
  padding: 30px 50px;
  
}

.mds-foot-list{
  padding: 0!important;
  list-style: none;

  li{
    line-height: 30px;

    i{
      margin-right: 20px;
    }
  }
}
</style>