<template>
  <div class="card">
    <img :src="disc.poster" />
    <h3>{{disc.title}}</h3>
    <h5>{{disc.author}}</h5>
    <h5>{{disc.year}}</h5>

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