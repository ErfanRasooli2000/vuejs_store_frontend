<script setup>

    import Search from './Search.vue'
    import Login from './Login.vue'
    import CartLogo from "./CartLogo.vue";

</script>

<template>
    <div class="w-full h-24 flex flex-row-reverse items-center header-border">
        <div class="w-1/3 flex flex-row-reverse">
            <div class="img-holder flex justify-center items-center w-1/4">
                <img v-bind:src="'./src/assets/logo-digital.png'" alt="LOGO">
            </div>
        </div>

        <Search class="w-1/3"/>

        <div class="flex w-1/3">
            <CartLogo class="mx-5 mt-2"/>
            <Login class="mx-5"/>
        </div>

    </div>
</template>

<style>
    .header-border
    {
        border-bottom: 1px solid #e3dede;
    }
</style>