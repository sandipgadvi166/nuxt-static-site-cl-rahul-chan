<template lang="">
    <div class="productWrapper" >
        <h3 class="productWrapper__title h4 text-muted text-uppercase">Our Product</h3>
         <b-container class="mx-2 mx-auto">
      
             <b-tabs content-class="mt-3" align="center" fill>
                    <Exide img="/static/product_photos/automative.svg"/>
                    <Amaze :img="img"/>
                    <okaya />
                    <microtek />
                      <Lloyd />
                      <bluestar />
                     <Western />
                      <cruise />
                     <daikin />
                  
            </b-tabs>
      </b-container>
    </div>
</template>
<script>
import Exide from '@/components/product/exide.vue'
import Amaze from '@/components/product/amaze.vue'
import okaya from '@/components/product/okaya.vue'
import microtek from '@/components/product/microtek.vue'
import Lloyd from '@/components/product/Lloyd.vue'
import bluestar from '@/components/product/bluestar.vue'
import western from '@/components/product/western.vue'
import cruise from '@/components/product/cruise.vue'
import daikin from '@/components/product/daikin.vue'

export default {
  data() {
    return {
      img: '_nuxt/static/product_photos/automative.svg',
    }
  },
  components: {
    Exide,
    Amaze,
    okaya,
    microtek,
    Lloyd,
    bluestar,
    western,
    cruise,
    daikin,
  },
}
</script>
<style lang="">
</style>