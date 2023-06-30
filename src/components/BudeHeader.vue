<template>
    <header>
        <div class="container">
            <nav class="navbar navbar-expand">
                <a href="" class="link navbar-brand mr-auto">
                    <img src="../assets/logo.svg" alt="Bude Treinamentos" class="img d-inline-block align-top" id="logo">Futebol Clube
                </a>

                <div class="links mr-2">
                    <a href="#" v-on:click.prevent="$emit('change-component', 'home')" class="btn mr-5">Inicio</a>
                    <a href="#" v-on:click.prevent="$emit('change-component', 'news')" class="btn mr-5">Noticias</a>
                    <a href="#" class="btn mr-5">Classificaçao</a>

                    <select name="champ" id="select-champ" class="form-control" v-on:change="$emit('select-champ', $event.target.value)">
                        <option value="">Selecione um campeonato</option>
                        <option value="Campeonato Brasileiro" selected>Campeonato Brasileiro</option>
                        <option value="Campeonato Espanhol">Campeonato Espanhol</option>
                        <option value="Campeonato Italiano">Campeonato Italiano</option>
                        <option value="Campeonato Inglês">Campeonato Inglês</option>
                    </select>
                </div>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {

    }
</script>

<style scoped>

    header{
        background-color: #000;
    }
    #logo{
        width: 150px;
        height: 100%;
    }
    .links{
        display: inline-flex;
    }
    .link{
        color: #d48e23;
        font-size: 30px;
        font-family: 'Rajdhani';
    }
    .links a{
        color: #fff;
    }
    .links a:focus{
        outline: none !important;
        box-shadow: none;
    }



</style>