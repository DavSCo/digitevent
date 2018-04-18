<template>
  <div>
      <div class="gallery-img-container" v-on:mouseenter="isHover=true" v-on:mouseleave="isHover=false">
                <img  :src="'https://picsum.photos/200/?random&element=' + d.id" alt="" width="100%" height="auto" class="gallery-img" />
                
                <div class="card-body body-article">
                  <p class="card-text grille-text">{{d.title | uppercase}}</p>
                  <span style="color:white;" v-show="isHover">{{d.body}}</span>
                </div>
              </div>
  </div>
</template>


<script>
export default {
    name: "card",
  data(){
      return {
          isHover: false,
      }
  },
  props: {
      d: Object
  }
}
</script>

<style lang="scss">
  @import '../assets/card.scss';
</style>
