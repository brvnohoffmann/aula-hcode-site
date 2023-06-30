<template>

    <section>
        <div class="container">
            <BudeSectionNewsIndividual
            v-for="notice in news"
            :key="notice.id"
            :img-name="notice.img"
            :img-info="notice.imgInfo"
            :news-title="notice.title"
            :news-date="notice.date">

            <template v-slot:title>
                <h2>{{notice.title }}</h2>
            </template>

            <p>{{ notice.content | truncate(200)}}</p>

            </BudeSectionNewsIndividual>
        </div>
    </section>
</template>

<script>
import BudeSectionNewsIndividual from './BudeSectionNewsIndividual.vue'


export default {
    components: {
        BudeSectionNewsIndividual
    },
    data(){
        return {
            news: []
        }
    },
    created(){
        this.news = [{
            id: 1,
            title: 'Começam os treinos para a nova temporada',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam excepturi aliquam animi qui quas enim laudantium error placeat labore, distinctio quaerat explicabo soluta ducimus tempora ipsam est non ratione? Qui? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sapiente vitae similique repudiandae doloribus quidem. Quibusdam illo atque corporis, dolorum optio doloribus recusandae. Animi, repellat. Porro sequi optio doloremque explicabo qui?',
            date: '1990/01/01',
            img: 'news1.jpg',
            imgInfo: 'Noticia 1'
        },{
            id: 2,
            title: 'Jogo de quarta termina empatado',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam excepturi aliquam animi qui quas enim laudantium error placeat labore, distinctio quaerat explicabo soluta ducimus tempora ipsam est non ratione? Qui? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sapiente vitae similique repudiandae doloribus quidem. Quibusdam illo atque corporis, dolorum optio doloribus recusandae. Animi, repellat. Porro sequi optio doloremque explicabo qui?',
            date: '1990/05/01',
            img: 'news2.jpg',
            imgInfo: 'Noticia 2'
        },{
            id: 3,
            title: 'A inauraçao do novo estádio sera semana q vem',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam excepturi aliquam animi qui quas enim laudantium error placeat labore, distinctio quaerat explicabo soluta ducimus tempora ipsam est non ratione? Qui? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sapiente vitae similique repudiandae doloribus quidem. Quibusdam illo atque corporis, dolorum optio doloribus recusandae. Animi, repellat. Porro sequi optio doloremque explicabo qui?',
            date: '1990/07/01',
            img: 'news3.jpg',
            imgInfo: 'Noticia 3'
        }]
    }

}
</script>

<style scoped>
section{
    padding: 50px 0;
    margin-block: 25px;
    background-color: #f37520;
}


</style>