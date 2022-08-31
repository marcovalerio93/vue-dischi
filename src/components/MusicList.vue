<template>
    <body class="my-bg-c">
        <div class="container ">
            <div class="row row-cols-5 g-8">    
            <MyDisc  v-for="disc in MusicList" :key="disc.index" :disc="disc"/>
            </div>
        </div>  
    </body>    
  
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
                that.MusicList = respone.data.response;
            }) 
            .catch(err=>{
                console.log(err);
            })
        }        
            
    }

}
</script>

<style lang="scss">
.my-bg-c{
    background-color: #1e2d3b;
}


</style>

