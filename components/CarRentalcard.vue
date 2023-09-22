<template class="">
    <div class="bg-[#F6F7F9]">

        <div class="  flex items-center max-lg:flex-col max-lg:gap-3 gap-[32px] container mx-auto">
            <div class="bg-[#54A6FF] flex-1 cartone-1 rounded-xl my-5 p-[24px] text-white flex flex-col items-start ">
                <span class=" text-3xl mb-2 w-[300px] font-semibold">The Best Platform</span>

                <span class="text-3xl  w-[300px] font-semibold">for Car Rental</span>
                <span class="text-lg  w-[300px] font-[400] mt-[16px]">Ease of doing a car rental safely and reliably. Of
                    course
                    at a low price.</span>
                <button class="button w-auto mt-3">
                    Rental Car
                </button>
                <div class="w-full flex items-center mt-3 justify-center">
                    <img src="../assets/car1.png" alt="" class="w-auto h-[100px]">
                </div>
            </div>
            <div class="bg-[#3563E9] flex-1 cartone-2 rounded-xl  my-5 p-[24px] text-white flex flex-col items-start ">
                <span class=" text-3xl mb-2 w-[300px] font-semibold">Easy way to rent a</span>

                <span class="text-3xl  w-[300px] font-semibold">car at a low price</span>
                <span class="text-lg  w-[300px] font-[400] mt-[16px]">Providing cheap car rental services and safe and
                    comfortable facilities.</span>
                <button class="button2 bg-[#54A6FF] w-auto mt-3">
                    Rental Car
                </button>
                <div class="w-full flex items-center  mt-3 justify-center">
                    <img src="../assets/car2.png" alt="" class="w-auto h-[100px]">
                </div>
            </div>
        </div>
        <div class="w-full my-3 container mx-auto cursor-pointer flex item-center justify-between text-[#90A3BF] text-sm">
            Popular Car
            <a class="hover:underline text-[#54A6FF] transition">
                View All
            </a>
        </div>
        <div class="container mx-auto my-3">
            <carousel class=" w-full py-3 " v-bind="settings" :breakpoints="breakpoints">
                <slide v-for="item in items" :key="item.id">
                    <CarCard />
                </slide>
            </carousel>
        </div>
        <div class="w-full my-3 container mx-auto cursor-pointer flex item-center justify-between text-[#90A3BF] text-sm">
            Recomendation Car

        </div>
        <div class="container mx-auto flex flex-wrap items-center justify-center ">

            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
            <CarCard />
        </div>
        <div class="container mx-auto flex items-center ">

            <button class="button w-auto mx-auto mt-3">
                Rental Car
            </button>
        </div>
    </div>
</template>
<style >
.container {
    padding: 1rem;
}

.cartone-1 {

    background-image: url("../assets/patterns.png");
    animation: animateScale 15s infinite ease-in-out;
}

.cartone-2 {

    background-image: url("../assets/patterns2.png");
    animation: animateScale 15s infinite ease-in-out;
}

.button {
    @apply border border-[#3563E9] bg-[#3563E9] w-auto rounded-lg text-white px-4 py-2 transition;

}

.button:hover {
    @apply border border-[#3563E9] bg-[white] text-[#3563E9];
}

.button:active {
    @apply scale-[0.95];
}

.button2 {
    @apply border border-[#54A6FF] bg-[#54A6FF] w-auto rounded-lg text-white px-4 py-2 transition;

}

.button2:hover {
    @apply border border-[#54A6FF] bg-[white] text-[#54A6FF];
}

.button2:active {
    @apply scale-[0.95];
}

/* .cartone-2 {
    background-image: url("../assets/BG.png");
    background-size: 105% 105%;
    background-position: 30% 30%;
    animation: Move 7s ease-in-out infinite;
} */

@keyframes animateScale {
    0% {
        background-size: 100%;
    }

    25% {
        background-size: 110%;

    }

    50% {
        background-size: 120%;

    }

    75% {
        background-size: 110%;
    }

    100% {
        background-size: 100%;

    }
}

@keyframes Move {
    0% {
        background-position: 0% 0%;
    }

    25% {
        background-position: 100% 0%;
    }

    50% {
        background-position: 120% 0%;

    }

    75% {
        background-position: 100% 0%;
    }

    100% {
        background-position: 0% 0%;
    }
}
</style>

<script>
import { Carousel, Slide } from 'vue3-carousel';
import "vue3-carousel/dist/carousel.css";
export default {
    components: {
        Carousel,
        Slide,
    },
    data() {
        return {
            items: [
                { id: 1, image: 'path-to-image-1.jpg' },
                { id: 2, image: 'path-to-image-2.jpg' },
                { id: 3, image: 'path-to-image-2.jpg' },
                { id: 5, image: 'path-to-image-2.jpg' },
                { id: 5, image: 'path-to-image-2.jpg' },
                { id: 5, image: 'path-to-image-2.jpg' },
                // Add more items as needed
            ],

            // carousel settings
            settings: {

                snapAlign: 'center',
            },
            // breakpoints are mobile first
            // any settings not specified will fallback to the carousel settings
            breakpoints: {
                640: {
                    itemsToShow: 1.5,
                    snapAlign: 'start',
                },
                768: {
                    itemsToShow: 2,
                },
                1024: {
                    itemsToShow: 3,
                },
                1280: {
                    itemsToShow: 4,
                },
            },

        };
    },
};
</script>