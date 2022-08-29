<template>
  <div>
    <MyDisc v-for="disc in MyDisc" :key="disc.id" :disc="disc"/>

  </div>
</template>

<script>
import axios from 'axios';

import MyDisc from './MyDisc.vue';

export default {
    name: 'MusicList',
    components: {
        MyDisc,
    },

    data() {
        return {
            MusicList:[],
            endpoint: 'https://flynn.boolean.careers/exercises/api/array/music'
        }
    },
    created() {
        this.getMusicList();
        
    },
    methods:{
        getMusicList (){
            let that = this;
            axios.get(this.endpoint)
            .then(function (respone){
                that.MusicList = respone.data;
            }) 
            .catch(err=>{
                console.log(err);
            })
        }        
            
    }

}
</script>

<style>

</style>

