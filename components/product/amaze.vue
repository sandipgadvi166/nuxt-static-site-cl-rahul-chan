<template lang="">
    <b-tab no-body title="Amaze">
                        <div class="pa-5 mb-5 mx-auto">
                            <b-row class="p-3">
                                <b-col class="mt-5">
                                <div>
                                   <item :img="this.img"/>
                                </div>
                                </b-col>
                            </b-row>
                        </div>
                  </b-tab>
</template>
<script>
import item from '@/components/product/item/item.vue'

export default {
  props: ['img'],
  components: {
    item,
  },

  mounted() {
    console.log(this.img)
  },
}
</script>
<style lang="">
</style>