<template>
  <div>
    <h3 class="text-center h4 text-muted text-uppercase">Gallery</h3>
    <div class="gallery">
      <div>
        <b-carousel
          class="text-black"
          id="carousel-fade"
          style="text-shadow: 0px 0px 2px #000"
          fade
          controls
          indicators
        >
          <div v-for="imgs in img" :key="imgs.src">
            <b-carousel-slide :img-src="imgs.src"></b-carousel-slide>
          </div>
        </b-carousel>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      img: [
        {
          src: 'office_photos/office.png',
        },
        {
          src: 'office_photos/office2.png',
        },
      ],
    }
  },
}
</script>
<style lang="">
</style>