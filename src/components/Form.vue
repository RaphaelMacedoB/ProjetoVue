<template>
    <div>
        <h2>Meu formulário</h2>
    <form action="" @submit="enviarFormulario($event)">
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <Submit />
        </div>
        
    </form>
    <p>Conteúdo</p>
    </div>
</template>
<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'
export default {
    name: "Form",
    components: {
        InputText,
        Submit
    },
    data() {
        return {
            name: "",
            email:""
        }
    },
    methods:{
        enviarFormulario(e){

            const name = this.name;
            const email = this.email;

            e.preventDefault();
            console.log("Formulário enviado !")
            console.log("O nome é " + name)
            console.log("O email é " + email)

            // Requisição para inserir no banco os dados

        }
    }
}
</script>
<style scoped>
    p{
        margin: 150px;
    }
</style>