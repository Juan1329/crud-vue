<template>
    <div>
        <input type="email" v-model="email" placeholder="email">
        <input type="text" v-model="nome" placeholder="nome">
        <input type="password" v-model="senha" placeholder="senha">
        <input type="submit" v-on:click="pronto" value="pronto">
        <input type="submit" v-on:click="voltar" value="voltar">
    </div>
</template>
<script>
export default {
    data(){
        return{
            email: '',
            nome: '',
            senha: '',
            infos: '',
            teste: ''
        }
    },
    methods: {
        pronto(){
            this.infos = 'Cadastrado: '+ this.email + this.nome + this.senha; 
        },
        voltar(){
            this.$router.push()
        }
    }
}
</script>
