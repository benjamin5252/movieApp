<template>
  <!-- Hero -->
  <div class="home">
    <Hero />
    <div class="container movies">
      <div id="movie-grid" class="movie-grid">
        <div v-for="(movie, index) in movies" :key="index" class="movie">
          <div class="movie-img">
            haha
            <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`" alt="gg">
            <p class="review">{{movie.vote_average}}</p>
            <p class="overview">{{movie.vote_average}}</p>
          </div>
          <div class="info">
            <p class="title">
              {{movie.title.slice(0,25)}} <span v-if="movie.title.length > 25">...</span>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  
</template>

<script>
import axios from 'axios'
export default {
  name: 'IndexPage',
  data() {
    return {
      movies: [],
    }
  },
  methods: {
    async getMovies() {
      const data = axios.get('https://api.themoviedb.org/3/movie/now_playing?api_key=ba9e810f75de1fbaf29ce1f3351c8426&language=en-US&page=1')
      const result = await data
      result.data.results.forEach(movie => {
        this.movies.push(movie)
      })
      console.log(this.movies)
    }
  },
  async fetch() {
    await this.getMovies()
  }
}
</script>
