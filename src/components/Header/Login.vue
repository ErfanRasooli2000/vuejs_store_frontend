<template>
    <div v-on:click="clicked" class="flex flex-row-reverse p-2.5 px-5 rounded-2xl border border-gray-200 hover:cursor-pointer select-none">
        <i class="bi bi-person-circle text-2xl mt-0.5"></i>
        <p class="mt-1.5 mr-2 text-sm">ورود / ثبت نام</p>
    </div>
</template>

<script>
export default {
    name: "Login" ,
    methods:
        {
            clicked(){
            }
        }
}
</script>

<style scoped>

</style>