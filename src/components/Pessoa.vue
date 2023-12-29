<template>
    <div>
        <h2>Está é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email" :esta_trabalhando=false />
        <Form />
    </div>
</template>
<script>
import Info from './Info.vue';
import Form from './Form.vue';
export default{
    name: "Pessoa",
    components: {
        Info,
        Form
    },
    data() {
        return {
            nome: "Raphael",
            email: "faeldojo2@gmail.com"
        }
    },
}
</script>