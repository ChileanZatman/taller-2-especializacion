<template lang="">
    <div class="col">
               <div class="card bg-dark text-white my-3 " style="height: auto; width: 100%">
                   <img v-bind:src="'https://image.tmdb.org/t/p/w500/' + movie.poster_path" class="card-img img-fluid" style="width: 100%; height: 15vw; object-fit: cover;" >
                   <div class="card-img-overlay" style="background-color: darkgrey; filter: opacity(0.25);">
                        
                   </div>
                   <h5 class="card-title">{{movie.title}}</h5>
                    <p class="card-text">avg {{movie.vote_average}}</p>
                    <router-link v-bind:to="'/movie/'+ movie.id" class="stretched-link"/>
               </div>
            </div>
</template>
<script>
export default {
    name: 'movie-card',
    props: {
        movie: {
            type: Object,
            required: true,
        }
    },
    
}
</script>
<style lang="">
    
</style>