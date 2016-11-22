<template>
  <div class="sharepear-gallery">
    <sharepear-picture
      v-for="picture in gallery"
      v-bind:width="picture.width"
      v-bind:height="picture.height"
      v-bind:url="picture.url">
    </sharepear-picture>
  </div>
</template>

<script type="text/babel">
  import SharepearPicture from './SharepearPicture.vue'
  import { getPicturesSize } from 'sharepear-gallery'

  export default {
    props: {
      pictures: Array,
      galleryWidth: Number,
      viewportHeight: Number
    },
    computed: {
      gallery: function () {
        return getPicturesSize(this.galleryWidth, this.viewportHeight, this.pictures)
      }
    },
    components: {
      SharepearPicture
    }
  }
</script>

<style>
.sharepear-gallery {
  font-size: 0;
  margin: 4px;
}
</style>
