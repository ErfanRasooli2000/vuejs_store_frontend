<script>
    export default {
       name : "underSlider",
        data(){
            return{
                datas : [
                    {name : "ارسال رایگان" , underName: " در سفارش‌های بیشتر از ۲۰۰ هزار تومان" , icon : "bi bi-truck"},
                    {name : "پرداخت در محل" , underName: " در تهران و بزودی در سراسر کشور" , icon : "bi bi-credit-card-2-back"},
                    {name : "سلامت کالا" , underName: " تضمین کیفیت محصولات" , icon : "bi bi-award"},
                    {name : "بهترین قیمت" , underName: " قیمت منصفانه و تخفیف هفتگی" , icon : "bi bi-tag mt-1"},
            ],
            }
        }
    }
</script>

<template>

    <div class="flex flex-row-reverse items-center justify-around">
        <div v-for="data in datas" class="flex flex-row-reverse items-center mt-8">
            <i :class="data.icon" class="text-5xl"></i>
            <div class="text-right mr-5">
                <p class="text-sm">{{data.name}}</p>
                <p class="text-sm mt-2">{{data.underName}}</p>
            </div>
        </div>
    </div>

</template>

<style>

</style>