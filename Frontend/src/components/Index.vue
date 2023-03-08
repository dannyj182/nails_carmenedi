<template>

  <section>
    <div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="../../public/img/1.png" class="d-block w-100" alt="img1">
        </div>
        <div class="carousel-item">
          <img src="../../public/img/2.png" class="d-block w-100" alt="img2">
        </div>
        <div class="carousel-item">
          <img src="../../public/img/3.png" class="d-block w-100" alt="img3">
        </div>
      </div>
    </div>
  </section>

</template>

<script>
  export default  {
    name: 'src-components-index',
    props: [],
    mounted () {
      if(this.$store.state.isLogin){
        this.$store.dispatch('lastActivity')
      }
    },
    beforeUpdate (){
      if(this.$store.state.isLogin){
        this.$store.dispatch('lastActivity')
      }
    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}
</script>

<style scoped lang="css">

</style>
