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
  <div id="head" class="flex-horizontal flex-center-align flex-space-between">
    <NuxtLink to="/" class="without-decoration secondary button">Volver</NuxtLink>
    <h1 id="s-title">Regístrate en <span id="s-ask">Ask</span>Matcom</h1>
    <a id="hide">
      <!--Para que quede el texto en el centro
      en el css le pongo el color igual al fondo
      -->
      Volver
    </a>

  </div>

  <div id="s-container-form">
    <slot/>
  </div>

</div>
</template>

<style scoped>

#head{
  width: 90%;
  margin-left: auto;
  margin-right: auto;
}

  #s-ask{
    color:var(--primary-color);
  }

#hide{
  color:var(--back-color);
}

#s-container-form{
  background:black;
}

</style>
