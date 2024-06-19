<script>
// Adicionando um comentário aleatório
    export default {
        props: ({
            titulo: {
                type: String,
                required: true
            },
            logo: {
                type: String,
                required: true
            },
        }),
        methods: ({
            irParaLogin() {
                this.$router.push('/login')
            },
        })
    }
</script>

<template>
    <nav>
        <div id="cab">
            <div id="div_logo">
                <span>
                    <img :src="logo" >
                </span>
            </div>
            <div id="login">
                <button id="b" class="btn btn-primary" @click="irParaLogin">
                    Sair
                </button>
            </div>
            <div id="div_titulo">
                <span>{{ titulo }}</span>
            </div>
        </div>
    </nav>
</template>

<style scoped>
    nav {
        background-color: white;
        color: white;
        padding: 20px;
        right: 0px;
        width: 100%;
        position: absolute;
        top: 0px;
    }
    #cab{
        display: flex;
        justify-content: space-between;
    }
    #div_logo{
        display: flex;
        align-items: center;
        margin: auto;
    }
    #div_titulo{
        color:black;
    }
    #login{
        text-align: right;
        width: 100%;
    }
    #b{
        width: 75px
    }
</style>