<template>
  <h1>{{ topicId }}</h1>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    topicId: {
      type: String,
      required: true
    }
  }
})
</script>
