<template>
  <div>
    <h3 class="text-center h4 text-muted text-uppercase">Gallery</h3>
    <b-container>
      <div class="gallery" ref="wdd">
        <div>
          <b-carousel
            class="text-black"
            id="carousel-fade"
            style="text-shadow: 0px 0px 2px #000"
            fade
            controls
          >
            <div v-for="imgs in img" :key="imgs.src">
              <b-carousel-slide :img-src="imgs.src"></b-carousel-slide>
            </div>
          </b-carousel>
        </div>
      </div>
    </b-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      img: [],
      wd: '',
    }
  },
  mounted() {
    this.wd = this.$refs.wdd.clientWidth
    if (this.wd > 576) {
      this.img.push(
        {
          src: 'office_photos/office.png',
        },
        {
          src: 'office_photos/office2.png',
        }
      )
    } else {
      this.img.push({
        src: 'office_photos/mobile_office.png',
      })
    }
  },
}
</script>
<style lang="">
</style>