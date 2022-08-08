<script setup>
  import nav_state from '~~/state/nav-state';
  const {title} = defineProps(['title'])
  useHead({
    title: title,
    // or, instead:
    // titleTemplate: (title) => `My App - ${title}`,
    viewport: 'width=device-width, initial-scale=1',
    htmlAttrs:{lang:'es'},
    charset: 'utf-8',
    meta: [
      { name: 'description', content: 'Sitio de dudas y sugerencias de la facultad de matemática y computación de la Universidad de La Habana' }
    ],
    link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.png' }]
})
</script>

<template>
<div>
    hola
  <slot/>
</div>
</template>
