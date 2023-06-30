<template>
    <div>

        <div class="container">
            <div class="row mt-5">
                <h3>Voce está vendo as noticias do: {{ champ }}</h3>
            </div>
        </div>

        <component v-bind:is="currentComponent"></component>
        

        <div class="container">
            <div class="row my-club mt-5">
                <div class="col-6">
                    <h2>Seu clube é {{ myClub }}</h2>
                </div>
                <div class="col-6">
                    <BudeInput v-model="myClub"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import BudeSectionBanner from './BudeSectionBanner.vue';
import BudeInput from './BudeInput.vue'



export default {
    components: {
    BudeSectionBanner,
    BudeSectionNews: () => import('./BudeSectionNews.vue'),//async component
    BudeInput
    },
    data (){
        return {
            myClub: 'Bude treinamentos'
        }
    },
    props: {
        champ: String,
        currentComponent: String
    }
}
</script>

<style scoped>

</style>