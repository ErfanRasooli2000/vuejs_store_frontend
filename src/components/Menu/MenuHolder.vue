<template>
    <div class="w-full h-24 flex flex-row-reverse items-center">
        <ProductCategory class="mr-8"/>

        <ul class="no-underline flex flex-row-reverse header-list mr-16 text-sm">
            <li class="text-blue-600"><a href="#">صفحه نخست</a></li>
            <li><a href="#">بلاگ</a></li>
            <li><a href="#">فروشگاه</a></li>
            <li><a href="#">سوالات متداول</a></li>
            <li><a href="#">قوانین و شرایط</a></li>
            <li><a href="#">حساب کاربری</a></li>
        </ul>
    </div>
</template>

<script>

    import ProductCategory from "./ProductCategory.vue";

export default {
    name: "MenuHolder",
    components: {ProductCategory}
}
</script>

<style scoped>
    .header-list li
    {
        margin: 15px;
        font-weight: bolder;
    }
</style>