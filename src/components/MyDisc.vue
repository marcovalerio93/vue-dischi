<template>
  <div class="col">

    <div class="card text-center text-bg-secondary p-3 my-5">
      <img :src="disc.poster" class="card-img-top p-1"/>
      <h3>{{disc.title}}</h3>
      <h5>{{disc.author}}</h5>
      <h5>{{disc.year}}</h5>
    </div> 
  </div>
</template>

<script>
export default {
    name: 'MyDisc',
    props: {
        disc:Object
    }

}
</script>

<style>

</style>