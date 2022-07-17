<script setup>
    const options = ref(
        [
            {id:0,text:"Inicio", link:"#container"},
            {id:1,text:"FAQ", link:"#faq"},
            {id:2,text:"Dashbord", link:"/dashbord"}
        ])
</script>

<template>
<NuxtLayout>
 
  <NavBar :options="options">
    <template #logo>
      <Logo/>
    </template>  
  </NavBar>
</NuxtLayout>
</template>