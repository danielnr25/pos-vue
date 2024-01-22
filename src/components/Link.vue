<script setup>
    import { RouterLink } from 'vue-router';
    defineProps({
        to: {
            type: String,
        }
    })

</script>

<template>
<RouterLink
  :to="{name: to}"
  class="rounded-md text-white font-bold bg-blue-800 px-10 py-2"
>
  <slot></slot>
</RouterLink>
</template>