<template lang="">
    <div>
        <b-card
                                  style="max-width: 20rem"
                                    :img-src="this.img"
                                    img-alt="Image"
                                    img-top
                                    tag="article"
                                   
                                    >
                        <icon>
                            <fa :icon="['fab','whatsapp']" />
                            </icon>
                            <icon>
                            <fa :icon="['fa','phone']" />
                            </icon>
                            <icon>
                            <fa :icon="['fa','envelope']" />
                            </icon>
                                    </b-card>
    </div>
</template>
<script>
export default {
  name: 'item',
  props: ['img'],
  mounted() {
    console.log(this.img)
  },
}
</script>
<style lang="">
</style>