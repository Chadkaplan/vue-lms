<template>
  <div>
    <v-img
      class="relative"
      src="https://picsum.photos/410/300?random"
      width="50rem"
    >
    </v-img>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return { currentTime: 0, ticker: undefined }
  },
  mounted() {
    this.tick()
  },
  methods: {
    tick() {
      this.ticker = setInterval(() => {
        this.currentTime++
        this.$emit('currentTime', this.currentTime)
      }, 1000)
    }
  }
})
</script>
