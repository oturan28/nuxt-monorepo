<script setup lang="ts">
import type { UiTheMessage } from '#components'

const theMessage = ref<InstanceType<typeof UiTheMessage> | null>()

onMounted(() => {
  console.log('theMessage', theMessage.value)
})

const config = useRuntimeConfig()
</script>

<template>
  <div>
    {{ config.public.apiBase }}
    <p>search</p>
    <p>search</p>
    <p>search</p>
    <UiTheMessage ref="theMessage" />
  </div>
</template>
