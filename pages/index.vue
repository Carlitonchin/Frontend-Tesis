<script setup>
    import nav_state from '~~/state/nav-state';
</script>

<template>
<NuxtLayout>
 
  <NavBar :options="nav_state('Inicio')">
    <template #logo>
      <Logo/>
    </template>  
  </NavBar>

  <PageHome/>

</NuxtLayout>
</template>