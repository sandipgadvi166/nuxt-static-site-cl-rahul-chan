<template lang="">
    <div class="testimonial">
      <b-container>
        <h3 class="text-center h4 text-uppercase py-4 text-muted">Testimonial</h3>
        <br />
        <b-row>
          <b-col v-for="cards in card" v-bind:key="cards.title">
           <b-card
              :title="cards.title"
              :img-src="cards.img_"
              img-alt="Image"
              img-top
              tag="article"
             
              class="mb-2"
            >
    <b-card-text>
      Some quick example text to build on the card title and make up the bulk of the card's content.
    </b-card-text>

    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
            </b-col>
          </b-row>
      </b-container>
        </div>
</template>
<script>
export default {
  data() {
    return {
      card: [
        {
          img_: '_nuxt/static/man.jpg',
          title: 'Rahul Gandhi',
        },
        {
          img_: '_nuxt/static/man.jpg',
          title: 'Sayli Pednekar',
        },
        {
          img_: '_nuxt/static/man.jpg',
          title: 'Tejal Pokale',
        },
      ],
    }
  },
}
</script>
<style lang="">
</style>