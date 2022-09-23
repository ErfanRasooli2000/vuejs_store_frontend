<template>
    <div class="w-11/12 mx-auto object-fit-contain relative">
        <i v-on:click="slideLeft" class="bi bi-chevron-compact-left absolute top-1/2 left-2 text-3xl text-white hover:text-blue-600 hover:cursor-pointer"></i>
        <i v-on:click="slideRight" class="bi bi-chevron-compact-right absolute top-1/2 right-2 text-3xl text-white hover:text-blue-600 hover:cursor-pointer"></i>
            <div id="dotsHolder" class="flex justify-between absolute slider-dots">
                <i v-for="banner in banners" :key="banner.id" v-on:click="dotClicked(banner.id)" :id="'dots'+banner.id" class="bi bi-dot text-4xl flex flex-row hover:cursor-pointer hover:text-white"></i>
            </div>
        <img v-bind:src=banners[current].image alt="banner" class="rounded-2xl">
    </div>
</template>

<script>
export default {
    name: "Slider",
    data(){
        return{
            banners : [
                {id : 0 , image : './src/assets/images/slider/banner1.webp'} ,
                {id : 1 , image : './src/assets/images/slider/banner2.jpg'} ,
                {id : 2 , image : './src/assets/images/slider/banner3.jpg'}
            ],
            current : 0
        }
    },
    mounted() {
        this.changeDotColor(0 , this.current);
    },
    methods :
    {
        slideRight()
        {
            let last = this.current;
            this.current+1===this.banners.length ? this.current = 0 : this.current++;
            this.changeDotColor(last , this.current);
        },
        slideLeft()
        {
            let last = this.current;
            this.current===0 ? this.current = this.banners.length - 1 : this.current--;
            this.changeDotColor(last , this.current);
        },
        changeDotColor(last , next)
        {
            last = 'dots' + last;
            next = 'dots' + next;

            document.getElementById(last).classList.remove('text-white');
            document.getElementById(last).classList.add('text-black');
            document.getElementById(next).classList.remove('text-black');
            document.getElementById(next).classList.add('text-white');
        },
        dotClicked(id)
        {
            this.changeDotColor(this.current,id);
            this.current = id;
        }
    }
}
</script>

<style scoped>

    .object-fit-contain img
    {
        object-fit: contain;
    }

    .slider-dots
    {
        position: absolute;
        bottom: 0;
        left: 50%;
    }

</style>