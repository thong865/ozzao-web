<template>
    <div>
        <swiper-container :slides-per-view="3" :space-between="spaceBetween" :centered-slides="true" :pagination="{
            hideOnClick: true
        }" :breakpoints="{
    768: {
        slidesPerView: 3,
    },
}" @progress="onProgress" @slidechange="onSlideChange">
            <swiper-slide> <img class="w-full rounded-xl"
                    src="https://images.unsplash.com/photo-1628358011850-0f4f335bfb88?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1112&q=80"></swiper-slide>
            <swiper-slide>Slide 2</swiper-slide>
            <swiper-slide>Slide 3</swiper-slide>
        </swiper-container>
    </div>
</template>
  
<script setup>
import { register } from 'swiper/element/bundle';

register();
const spaceBetween = 10;
const onProgress = (e) => {
    const [swiper, progress] = e.detail;
    console.log(progress)
};

const onSlideChange = (e) => {
    console.log('slide changed')
}
// export default function () {
//     setup() {
//         const spaceBetween = 10;
//         const onProgress = (e) => {
//             const [swiper, progress] = e.detail;
//             console.log(progress)
//         };

//         const onSlideChange = (e) => {
//             console.log('slide changed')
//         }

//         return {
//             spaceBetween,
//             onProgress,
//             onSlideChange,
//         };
//     }
// }
</script>