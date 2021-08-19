<template>
    <Header/>
    <div class="page-container">
      <Article
      v-for="article in articleArray"
      :title="article.title"
      :img="article.img"
      :key="article.title"
      v-on:click="clicker"
      />
    </div>
</template>

<script>
import Header from './components/Header.vue'
import Article from './components/Article.vue'

export default {
  name: 'App',
  data () {
    return {
      articleArray: [
        {
          title: "White duck steals bread",
          img: "https://images.unsplash.com/photo-1597840637868-417c13c7e962?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8ZHVja3xlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&w=1000&q=80"
        },
        {
          title: "Record fast duck swimming",
          img: "https://upload.wikimedia.org/wikipedia/commons/a/a1/Mallard2.jpg"
        },
        {
          title: "The most beatuful duck in the world",
          img: "https://nas-national-prod.s3.amazonaws.com/styles/hero_mobile/s3/nyc-mandarin-duck_holly-mascaro.jpg?itok=-UKJAxBT"
        },
        {
          title: "Flying duck",
          img: "https://www.outdoorlife.com/uploads/2021/07/28/duck-6126758_1920.jpg"
        },
        {
          title: "Ring-neck duck",
          img: "https://nas-national-prod.s3.amazonaws.com/styles/hero_cover_bird_page/s3/h_ring-necked-duck_004_spring_california_beckymatsubara_flickrcc-by-2.0_breeding-adult-male.jpg?itok=O1pv-1pJ"
        }
      ]
    }
  },
  components: {
    Header,
    Article
  },
  methods: {
    clicker () {
      console.log('clickerino works!')
    }
  }
}
</script>

<style>
  body {
    margin: 0;
    padding: 0;
    width: 100%;
    color: #222;
    font-family: Open-sans, sans-serif;
  }

  .page-container {
    width: 100%;
    max-width: 60rem;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    margin: auto;
    justify-content: space-evenly;
    align-items: center;
    align-content: center;
    padding: 2rem 2rem;
  }
</style>
