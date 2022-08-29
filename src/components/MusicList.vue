<template>
  <div>

  </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'MusicList',
    data() {
        return {
            MusicList:[]
        }
    },
    created() {
        let that = this;

        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then(function (respone){
            that.MusicList = respone.data;
        }); 



         
    }
}
</script>

<style>

</style>

