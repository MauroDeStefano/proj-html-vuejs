<template>
  <div>
    <Contacts />
    <Jumbotron /> 
  </div>
</template>

<script>
import Contacts from './Contacts.vue';
import Jumbotron from './Jumbotron.vue';

export default {
  name: "Header",
  components: {
    Contacts,
    Jumbotron
  }
}
</script>

<style lang="scss">

@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';

</style>