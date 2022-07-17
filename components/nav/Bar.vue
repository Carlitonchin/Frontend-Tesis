<template>
    <div id="container" class="flex-horizontal flex-center-align flex-space-between p2 p1-top-bottom">
    <slot name="logo"/>
    <h1 class="m0 p0">Hola</h1>
    </div>
</template>

<style scoped>
    #container
    {
        background: rgba(0, 0, 0, 0.281);
-webkit-box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
-moz-box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
box-shadow: -4px -26px 30px 21px rgba(0,0,0,0.75);
    }
</style>