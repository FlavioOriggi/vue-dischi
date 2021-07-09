<template>
  <div class="container">
    <div v-if="!dataLoading" class="row row-cols-5">
      <div v-for="(icon,i) in apiElements" :key="i" class="g-4">
        <IconItem :iconInfo="icon"/>
      </div>
    </div>    
  </div>
</template>


<script>
import axios from 'axios';
import IconItem from '@/components/IconItem.vue';

export default {
    name : 'Main',
    components: {
        IconItem        
    },
    data(){
        return{
        urlApi : 'https://flynn.boolean.careers/exercises/api/array/music',
        apiElements : [],        
        }
    },
    created(){
        this.loadApi();
    },
    methods: {
        loadApi(){
        axios
            .get(this.urlApi)
            .then(response => {
                this.apiElements = response.data.response;                     
            });
        }
    }
}
</script>


<style lang="scss">  
</style>