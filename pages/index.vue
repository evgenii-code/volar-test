<template>
  <div>
    <base-input-foo v-model="form.foo" />

    <base-input-value v-model="form.value" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import BaseInputFoo from '~/components/BaseInputFoo.vue'
import BaseInputValue from '~/components/BaseInputValue.vue'

export default defineComponent({
  name: 'IndexPage',

  components: {
    BaseInputFoo,
    BaseInputValue,
  },

  data() {
    return {
      form: {
        foo: '',
        value: '',
      },
    }
  },
})
</script>
