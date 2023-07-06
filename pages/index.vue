<template>
  <div>
    <some-component />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SomeComponent from '~/components/SomeComponent.vue'

export default defineComponent({
  name: 'IndexPage',

  components: {
    SomeComponent,
  },
})
</script>
