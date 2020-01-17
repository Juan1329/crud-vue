<template>
  <section class="container">
    <div>
      <input type="email" v-model="email">
      <input type="password" v-model="senha">
      <input type="submit" value="entrar" v-on="logar()">
      <input type="submit" value="cadastro" v-on="cadastro()">

    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  data(){
    return{
      email: "",
      senha: ""
    }
  },
  
  methods: {
    logar(){
      if(this.email === 'juan.com' && this.senha === '123')
      this.$router.push({path: '/home.vue'})
    },
    cadastro(){
      this.$router.push({path: '/cadastro.vue'})
    } 
  }


  
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

