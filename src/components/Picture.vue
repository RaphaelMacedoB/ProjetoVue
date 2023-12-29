<template>
    <img :src="avatar" :alt="descricao">
    <MudarImagem @mudar-imagem="trocarImagem"/>
</template>
<script>
import Reutilizacao from './Reutilizacao.vue';
import MudarImagem from './MudarImagem.vue';
export default{
    name: "Picture",
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: "Raphael Macedo"
        };
    },
    components: { Reutilizacao, MudarImagem },
    methods:{
        trocarImagem(){
            this.avatar = "/img/avatar2.png"
        }
    }
}
</script>