<template>
  <div id="app">
    <MyEmail :email="emailCasuale" />
    <MyEmailGenerator @generaEmailCasuale="setEmail" />
  </div>
</template>

<script>
import MyEmail from './components/MyEmail.vue';
import MyEmailGenerator from './components/MyEmailGenerator.vue';

export default {
  name: 'App',
  components: {
    MyEmail,
    MyEmailGenerator
    
  },
  data() {
    return {
      emailCasuale: 'info@pippo.com'
    }
  },
  methods: {
    setEmail(email) {
      this.emailCasuale = email;
    }
  }
}
</script>

<style lang="scss">


</style>
