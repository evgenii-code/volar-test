<template>
  <input v-model="fooLocal" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

const EVENT_NAME_V_MODEL = 'update:foo'

export default defineComponent({
  name: 'BaseInput',

  model: {
    prop: 'foo',
    event: EVENT_NAME_V_MODEL,
  },

  props: {
    foo: {
      type: String,
      required: true,
    },
  },

  computed: {
    fooLocal: {
      get(): string {
        return this.foo
      },
      set(value: string) {
        this.$emit(EVENT_NAME_V_MODEL, value)
      },
    },
  },
})
</script>

<style scoped></style>
