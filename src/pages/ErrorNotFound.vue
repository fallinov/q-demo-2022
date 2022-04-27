<template>
  <div class="fullscreen bg-blue text-white text-center q-pa-md flex flex-center">
    <div>
      <div style="font-size: 30vh">
        404
      </div>

      <div class="text-h2" style="opacity:.4">
        Ooups. Vous êtes perdu ?
      </div>

      <q-btn
        class="q-mt-xl"
        color="red"
        text-color="white"
        unelevated
        to="/"
        label="Maiiiiisonn"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ErrorNotFound'
})
</script>
