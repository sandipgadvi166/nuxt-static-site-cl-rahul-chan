<template>
  <div>
    <section>
      <div>
        <b-navbar
          v-b-scrollspy
          toggleable="lg"
          type="light"
          variant="light"
          fixed="top"
        >
          <b-container>
            <b-navbar-brand href="#home">
              <!-- <fa :icon="['fas', 'lightbulb']" /> -->
              <b class="companyName"
                ><strong>
                
                <b-img-lazy src="~/static/logo.png" class="logo"></b-img-lazy>
                </strong></b
              >
              <!-- <span class="small logo"
                ><small>Tech Solutions Pvt Ltd</small></span
              > -->
            </b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav class="ml-auto">
                <b-nav-item href="#home"> Home </b-nav-item>
                <b-nav-item href="#product" v-bind:class="productClass">
                  Product
                </b-nav-item>
                <b-nav-item href="#gallery">Our Gallery </b-nav-item>
                <b-nav-item href="#about"> About Us</b-nav-item>
                <!-- <b-nav-item href="#testimonial"> Testimonial </b-nav-item> -->
                <b-nav-item href="#contact"> Contact Us</b-nav-item>
              </b-navbar-nav>
            </b-collapse>
          </b-container>
        </b-navbar>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      productClass: '',
    }
  },
}
</script>
