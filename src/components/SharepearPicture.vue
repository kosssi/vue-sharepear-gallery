<template>
  <div class="sharepear-picture" :style="styleObject"></div>
</template>

<script type="text/babel">
  export default {
    props: {
      width: Number,
      height: Number,
      url: String
    },
    computed: {
      styleObject: function () {
        return {
          width: this.width + 'px',
          height: this.height + 'px',
          backgroundImage: 'url(\'' + this.url + '\')'
        }
      }
    }
  }
</script>

<style>
.sharepear-picture {
    background-color: #77c4a5;
    box-sizing: border-box;
    display: inline-block;
    background-size: cover;
    border: 2px solid white;
}
</style>
