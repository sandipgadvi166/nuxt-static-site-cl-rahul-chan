<template>
  <div>
    <navbar />
    <div v-if="loading" class="loader">
      <b-progress :max="max" height="0.8rem" variant="success">
        <b-progress-bar :value="value">
          <span
            ><strong
              ><small>{{ value }} / {{ max }}</small></strong
            ></span
          >
        </b-progress-bar>
      </b-progress>
      <transition name="home" mode="out-in">
        <div class="loading">
          <div class="loading__text">LOADING</div>
        </div>
      </transition>
    </div>
    <div v-if="mounted" class="bodyWrapper">
      <Nuxt />
    </div>
  </div>
</template>

<script>
export default {
  transition: {
    name: 'home',
    mode: 'out-in',
  },
  data() {
    return {
      mounted: false,
      loading: true,
      value: 1,
      max: 100,
    }
  },
  mounted() {
    for (let i = 0; i < this.max; i++) {
      setTimeout(() => {
        this.value = i
      }, 100)
    }
    setTimeout(() => {
      ;(this.loading = false), (this.mounted = true)
    }, 900)
  },
}
</script>
