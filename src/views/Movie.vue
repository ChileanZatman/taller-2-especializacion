<template lang="">
    <div class="vh-100">
        <div class="row pt-3">
            <div class="col-4">
                <img v-bind:src="'https://image.tmdb.org/t/p/w500/' + movie.poster_path" class="img-fluid " style="width: 100%; object-fit: cover;" >
            </div>
            <div class="col">
                <ul class="list-group list-group-flush pt-5">
                    <div>
                        <h4>Title</h4>
                        <li class="list-group-item">{{movie.title}}</li>
                    </div>
                    <div>
                        <h4>Popularity score</h4>
                        <li class="list-group-item">{{movie.popularity}}</li>
                    </div>
                    <div>
                        <h4>Score average</h4>
                        <li class="list-group-item">{{movie.vote_average}}</li>
                    </div>
                </ul>
            </div>
        </div>
        
    </div>
</template>
<script>
import apiService from '../services/api.service.js';
export default {
    name : 'Movie',
    
    data () {
        return {
            movie : {},
            id : this.$route.params.id
        }
    },
    mounted() {
        this.getMovie(this.id);
    },
    methods : {
        getMovie (id) {
            apiService.getMovie(id)
                .then(response => {
                    this.movie = response.data;
                })
                .catch(error => {
                    console.log(error);
                });
        },
        
    },
}
    

</script>
<style lang="">
    
</style>