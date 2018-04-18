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



<style  scoped>
.article {
  border-radius: 0 !important;
}

.image-article {
  border-top-left-radius: 0 !important;
  border-top-right-radius: 0 !important;
}
.body-article {
  background-color: #2e3443;
}
.grille-text {
  font-family: "Roboto", sans-serif;
  color: #d4eee2;
  text-align: end;
}
.grille-title {
  font-family: "Roboto", sans-serif;
  color: #d4eee2;
}
gallery {
  -webkit-column-count: 4;
  -moz-column-count: 4;
  column-count: 4;
  -webkit-column-gap: 10px;
  -moz-column-gap: 10px;
  column-gap: 10px;
  margin-top: 10px;
  overflow: hidden;
}

.gallery .gallery-img-container {
  width: 100%;
  height: auto;
  transition: 500ms;
  margin-bottom: 10px;
  page-break-inside: avoid; /* For Firefox. */
  -webkit-column-break-inside: avoid; /* For Chrome & friends. */
  break-inside: avoid; /* For standard browsers like IE. :-) */
}

.gallery .gallery-img-container:hover {
  opacity: 0.80;
}
</style>

