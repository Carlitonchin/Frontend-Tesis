<script setup>
    const props = defineProps(["options"])
</script>
<template>
    <div id="container" class="flex-horizontal flex-center-align flex-space-between p2 p1-top-bottom">
        <slot name="logo"/>
        <div id="container-options" class="flex-horizontal flex-space-between">
            <NuxtLink class="clickable without-decoration s-link"
            v-for="item in props.options" :key="item.id" :to="item.link">
            <h2 >
                {{item.text}}
              </h2> 
            </NuxtLink>
               
        </div>

        <div class="flex-horizontal flex-center-align">
            <div id="login" class="button secondary">
                Iniciar Sesión
            </div>
            <div class="button primary">
                Registrarse
            </div>
        </div>

    </div>
</template>

<style scoped>
    #container
    {
        background: rgba(0, 0, 0, 0.281);
        -webkit-box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
        -moz-box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
        box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
        height: 8vh;
        min-height: 40px;
    }

    #login
    {
        margin-right: 0.5rem;
    }

    #container-options
    {
        width: 30%;
    }

    .s-link
    {
        transition: 100ms ease-in-out;
    }
    .s-link:hover
    {
        color:var(--primary-color)
    }
</style>