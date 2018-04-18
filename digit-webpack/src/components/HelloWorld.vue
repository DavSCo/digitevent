<template>
  <div class="hello">
    <div class="container-fluid">
      <div class="row">
        <div class="col">

        </div>

      </div>
      <div class="row">
        <div class="container-fluid">
          <div class="gallery">
            <div style=" margin-bottom: 20px;height: 88px;" class="card article">
              <div class="card-body body-article">
                <h5 class="card-text grille-title">
                  ILLUSTRATIONS BY
                  <h5 style="color:#C42F4A">RYO TAKEMASA</h5>
                </h5>

              </div>
            </div>
            <div v-if="data.length > 0" v-for="d in data" :key="d.id">
              <Card :d="d" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.0/umd/popper.min.js" integrity="sha384-cs/chFZiN24E4KMATLdqdvsezGxaGsi4hLGOzlXwp5UZB1LY//20VyM2taTB4QvJ" crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/js/bootstrap.min.js" integrity="sha384-uefMccjFJAIv6A+rW+L4AHf99KvxDjWSu1z9VI8SKNVmz4sk7buKt/6v9KI65qnm" crossorigin="anonymous"></script>
<script>
import Card from "./Card";
export default {
  name: "HelloWorld",
  components: {Card},
  data() {
    return {
      isHover: false,
      data: []
    };
  },
  props: {
    msg: String
  },
  created() {
    fetch("https://jsonplaceholder.typicode.com/posts")
      .then(res => res.json())
      .then(json => (this.data = json));
  }
};
</script>


<style lang="scss">
  @import '../assets/main.scss';
</style>
