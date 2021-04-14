<template lang="">
  <div ref="wd" class="mainslider" >
     <div class="star">
          
            <b-img-lazy fluid src="~/static/images/star.png"></b-img-lazy>

            </div>
            <div class="star2">
          
            <b-img-lazy fluid src="~/static/images/star.png"></b-img-lazy>

            </div>
            <div class="star3">
          
            <b-img-lazy fluid src="~/static/images/star.png"></b-img-lazy>

            </div>
            <div class="star4">
          
            <b-img-lazy fluid src="~/static/images/star.png"></b-img-lazy>

      </div>
    <div class="slogn">
 <h1 class="text-center">
      Life made simple
   </h1>
   <p>
     Get all your Industrial & home appliances @one place
     <li>Air Conditioners</li>
     <li>Refrigerators</li>
     <li>industiral Battery</li>
     <li>Home UPS</li>
     
   </p>
   <b-button>CONTACT</b-button>
      </div>
    <div class="sofa">
      <b-img-lazy fluid src="~/static/images/sofa.png"></b-img-lazy>
    </div>

    <div class="components">
            <div class="ac">
            <b-img-lazy fluid src="~/static/icons/blue.png"></b-img-lazy>
            <!-- <b-img-lazy class="wind" fluid src="~/static/images/ac_wind.png"></b-img-lazy> -->
          </div>
          <div class="powercode">
            <b-img-lazy fluid src="~/static/images/powercode.png"></b-img-lazy>

            </div>
            <div class="exideBattery">
            <b-img-lazy fluid src="~/static/icons/exide.png"></b-img-lazy>

            </div>
            <div class="exideBattery2">
            <b-img-lazy fluid src="~/static/icons/amaze.png"></b-img-lazy>

            </div>
            <div class="exideBattery3">
            <b-img-lazy fluid src="~/static/icons/okaya.png"></b-img-lazy>

            </div>
            <div class="exideBattery4">
            <b-img-lazy fluid src="~/static/icons/microtek.png"></b-img-lazy>

            </div>
      </div>
   
         
      

  <!-- <b-carousel
  class="text-black"
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    controls
    indicators
    
  > 
  <div v-for="imgs in img" >
  <b-carousel-slide :img-src="imgs"></b-carousel-slide>
  </div>
 </b-carousel> -->
      <!-- <b-img-lazy class="mainslider__earth" :src="earth" alt="Image 1"></b-img-lazy> -->
</div>
</template>
<script>
export default {
  data() {
    return {
      wd: '',
      img: [],
      earth: 'earth.png',
    }
  },
  mounted() {
    this.wd = this.$refs.wd.clientWidth
    console.log(this.wd)
    if (this.wd > 576) {
      this.img.push(['slider-2.png'])
    } else {
      this.img = ['mb_Profile_banner.png', 'mb_Profile_banner.png']
    }
  },
}
</script>
