<template>
  <input v-model="valueLocal" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

const EVENT_NAME_V_MODEL = 'update:value'

export default defineComponent({
  name: 'BaseInput',

  model: {
    prop: 'value',
    event: EVENT_NAME_V_MODEL,
  },

  props: {
    value: {
      type: String,
      required: true,
    },
  },

  computed: {
    valueLocal: {
      get(): string {
        return this.value
      },
      set(value: string) {
        this.$emit(EVENT_NAME_V_MODEL, value)
      },
    },
  },
})
</script>

<style scoped></style>
