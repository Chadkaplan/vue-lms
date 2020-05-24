<template>
  <h1>{{ currentTime }}</h1>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    topicId: {
      type: String,
      required: true
    },
    currentTime: {
      type: Number,
      required: true
    }
  }
})
</script>
