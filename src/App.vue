<template>
  <div id="app">
    <sharepear-gallery
      v-bind:pictures="pictures"
      v-bind:galleryWidth="galleryWidth"
      v-bind:viewportHeight="viewportHeight"></sharepear-picture>
  </div>
</template>

<script>
import SharepearGallery from './components/SharepearGallery.vue'

export default {
  name: 'app',
  components: {
    SharepearGallery
  },
  data: function () {
    return {
      galleryWidth: window.innerWidth,
      viewportHeight: document.documentElement.clientHeight,
      pictures: [
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=27' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=36' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=29' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=37' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=38' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=32' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=33' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=7' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=34' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=35' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=10' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=11' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=12' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=13' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=14' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=15' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=16' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=17' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=18' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=19' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=20' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=21' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=22' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=23' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=24' },
        { width: 800, height: 531, url: 'https://unsplash.it/800/531/?image=25' },
        { width: 531, height: 800, url: 'https://unsplash.it/531/800/?image=26' }
      ]
    }
  },
  ready: function () {
    this.galleryWidth = this.$el.parentElement.offsetWidth
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
