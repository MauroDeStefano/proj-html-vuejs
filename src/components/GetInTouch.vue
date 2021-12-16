<template>
  <div class="container py-5">
    <div class="row py-5">
      <div class="col-8">
        <p class="text-emp mds-text-wide-s fw-bolder">SEND A MESSAGE</p>
        <h2 class="mb-3 fw-bolder mds-title-wide">Get in <span class="text-emp bg-text-emp px-2 rounded ">Touch</span></h2>
        <p class="mds-text-gray">We will respond to your message as soon as possible.</p>
        <!-- FAKe form -->
        <input type="text" placeholder="Name" class="mds-right-margin my-3 rounded"><input type="text" placeholder="Email" class="rounded">
        <input type="text" placeholder="Phone" class="mds-right-margin mb-3 rounded"><select name="" id="selectioninfo" class="rounded">
          <option value="">More info</option>
          <option value="">Demand Catalouge</option>
          <option value="">Job Oportunities</option>
        </select>
        <textarea name="" placeholder="Message" id="text-message" class="rounded"></textarea>
        <a class="btn btn-info mds-btn mt-4 ">SEND</a>
      </div>
      <div class="col-4">
        <h4 class="fw-bolder mb-4">Example Inc.</h4>
        <p class="mds-text-gray">Lorem ipsum sit amet, consectetur adipiscing elit.</p>
        <p class="mds-text-gray">Praesent diam lacus, dapibus sed imperdiet consectetur.</p>
        <!-- cycle of the company info, same as in the header -->
        <div class="mds-primary-color " v-for="(item, index) in contacts" :key=index>
          <p class="mb-3"><i :class="item.phone.logo"></i> {{item.phone.content}}</p>
          <p class="mb-3"><i :class="item.mail.logo"></i> {{item.mail.content}}</p>
          <p><i :class="item.address.logo"></i> {{item.address.content}}</p>
        </div>
      <a href="https://www.google.it/maps/place/Boolean+SRLS/@45.4616341,9.1334771,17z/data=!3m1!4b1!4m5!3m4!1s0x4786c22ab05c3bbf:0xa481aa5be8d54a11!8m2!3d45.4616481!4d9.1357369" class="btn mds-btn-empty mds-primary-color" target="_blank">VIEW MAP</a>
      </div>
    </div>
  </div>
</template>

<script>
import contacts from '../assets/data/contatcs.js';

export default {
  name: "GetInTouch",
  data(){
    return{
      contacts
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';


input, select, textarea{
  width: calc(100% / 2 - 5px);
  background-color: #ECECEC;
  color: gray;
  border-style: none;
  padding-left: 15px;
}

input, select{
  line-height: 40px;
  height: 40px;
}

select{
  color: #b8b6b6;
}

textarea{
  width: 100%;
  height: 150px;
  background-color: #ECECEC;
  resize: none!important;
  padding-top: 7px;
}

.mds-right-margin{
  margin-right: 10px;
}

.mds-primary-color{
  p{
    font-size: 20px;

    i{
      padding: 15px;
      margin-right: 10px;
      background-color: #DAECED;
      border-radius: 50%;
    }
  }
}
</style>