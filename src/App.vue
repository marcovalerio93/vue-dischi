<template>
  <div id="app">
    <MyHeader/>
    <MusicList/>
    

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MusicList from './components/MusicList.vue';


export default {
  name: 'App',
  components: {
    MyHeader,
    MusicList,
  }
}
</script>

<style lang="scss">

 @import '@/styles/general.scss'

</style>
