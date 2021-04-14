<template>
  <div>
    <section id="home">
      <slider />
    </section>
    <section>
      <menu />
    </section>
    <section id="distribution">
      <b-container>
        <h3 class="text-center">our distributions</h3>
        <b-row>
          <b-col>
            <a href="#product">
              <b-img-lazy  src="~/static/icons/exide.png" /></b-img-lazy>
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class="" src="~/static/icons/amaze.png" />
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class="" src="~/static/icons/microtek.png" />
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class="" src="~/static/icons/okaya.png" />
            </a>
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <a href="#product">
              <b-img class=""  src="~/static/icons/air.png" />
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class=""  src="~/static/icons/blue.png" />
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class=""  src="~/static/icons/cruise.png" />
            </a>
          </b-col>
          <b-col>
            <a href="#product">
              <b-img class=""  src="~/static/icons/daikin.png" />
            </a>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="product">
      <Product />
    </section>
    <section id="gallery" style="overflow: hidden">
      <Gallery />
    </section>
    <section id="about">
      <About />
    </section>
    <!-- <section id="testimonial">
      <testimonial />
    </section> -->
    <section id="contact">
      <Contact />
    </section>
    <section>
      <div class="footer">
        <div class="footer__icons">
          <div>
           <a href="tel:919890038245">
             <fa :icon="['fas', 'phone']" :style="{ color: 'white' }" />
          </a> 
          </div>
          <div>
            <a href="https://api.whatsapp.com?phone='919890038245'&text='hello'">
              <fa :icon="['fab', 'whatsapp']" :style="{ color: 'white' }" />

            </a>
            
          </div>
          <div>
            <a href="mailto:bpsichalkaranji@gmail.com">
            <fa :icon="['fas', 'envelope']" :style="{ color: 'white' }" /></a>
          </div>
          <div>
            <a href="smstest://my-test">
            <fa :icon="['fas', 'comment-dots']" :style="{ color: 'white' }" /></a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import slider from '~/components/slider/slider.vue'
import menu from '~/components/menus/menu.vue'
import Gallery from '~/components/gallery/gallery.vue'
import Contact from '~/components/contact/contact.vue'
import Product from '~/components/products/product.vue'
import Footer from '~/components/footer/footer.vue'
import About from '~/components/about/about.vue'
import Testimonial from '~/components/testimonial/testimonial.vue'
import Distribution from '~/components/ourdistribution/distribution.vue'

export default {
  components: {
    slider,
    menu,
    Product,
    Contact,
    Footer,
    Gallery,
    About,
    Testimonial,
    Distribution,
  },
}
