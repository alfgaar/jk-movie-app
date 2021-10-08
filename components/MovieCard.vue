<template>
  <div class="movie">
    <div class="movie-img">
      <img :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`" alt />
      <p class="review">{{ movie.vote_average }}</p>
      <p class="overview">{{ movie.overview }}</p>
    </div>
    <div class="info">
      <p class="title">
        {{ movie.title.slice(0, 25) }}
        <span v-if="movie.title.length > 25">...</span>
      </p>
      <p class="release">
        Released:
        {{
          new Date(movie.release_date).toLocaleString('en-us', {
            month: 'long',
            day: 'numeric',
            year: 'numeric',
          })
        }}
      </p>
      <NuxtLink
        :to="{ name: 'movies-movieid', params: { movieid: movie.id } }"
        class="button button-light"
      >Get More info</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    movie: {
      type: Object,
      default() {
        return {
          adult: false,
          backdrop_path: '/70AV2Xx5FQYj20labp0EGdbjI6E.jpg',
          genre_ids: [28, 80, 53],
          id: 637649,
          original_language: 'en',
          original_title: 'Wrath of Man',
          overview: "A cold and mysterious new security guard for a Los Angeles cash truck company surprises his co-workers when he unleashes precision skills during a heist. The crew is left wondering who he is and where he came from. Soon, the marksman's ultimate motive becomes clear as he takes dramatic and irrevocable steps to settle a score.",
          popularity: 567.887,
          poster_path: '/M7SUK85sKjaStg4TKhlAVyGlz3.jpg',
          release_date: '2021-04-22',
          title: 'Wrath of Man',
          video: false,
          vote_average: 7.8,
          vote_count: 2375
        }
      }
    },
  },
}
</script>

<style lang="scss" scoped>
.movie {
  position: relative;
  display: flex;
  flex-direction: column;
  .movie-img {
    position: relative;
    overflow: hidden;
    &:hover {
      .overview {
        transform: translateY(0);
      }
    }
    img {
      display: block;
      width: 100%;
      height: 100%;
    }
    .review {
      position: absolute;
      top: 0;
      left: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 40px;
      height: 40px;
      background-color: #c92502;
      color: #fff;
      border-radius: 0 0 16px 0;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
        0 2px 4px -1px rgba(0, 0, 0, 0.06);
    }
    .overview {
      line-height: 1.5;
      position: absolute;
      bottom: 0;
      background-color: rgba(201, 38, 2, 0.9);
      padding: 12px;
      color: #fff;
      transform: translateY(100%);
      transition: 0.3s ease-in-out all;
    }
  }
  .info {
    margin-top: auto;
    .title {
      margin-top: 8px;
      color: #fff;
      font-size: 20px;
    }
    .release {
      margin-top: 8px;
      color: #c9c9c9;
    }
    .button {
      margin-top: 8px;
    }
  }
}
</style>
