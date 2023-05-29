<template>
    <div class="flex flex-col justify-around  h-[210px] mt-2 w-1/2">
        <div class="relative   bg-cover  w-[88%] h-4/5 rounded-[15px] " :style="{ backgroundImage: `url(${image})` }">
            <div class="w-8 h-8 bg-white rounded-full flex items-center justify-center absolute top-2 right-3">
                <svg class="w-6 h-6 text-gray-800" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M9.653 16.915l-.005-.003-.019-.01a20.759 20.759 0 01-1.162-.682 22.045 22.045 0 01-2.582-1.9C4.045 12.733 2 10.352 2 7.5a4.5 4.5 0 018-2.828A4.5 4.5 0 0118 7.5c0 2.852-2.044 5.233-3.885 6.82a22.049 22.049 0 01-3.744 2.582l-.019.01-.005.003h-.002a.739.739 0 01-.69.001l-.002-.001z">
                    </path>
                </svg>
            </div>
        </div>
        <p class="text-sm text-gray-400 mt-3">Blue Jeans</p>
        <p class="relative text-slate-800 font-bold text-xl w-full"><span class="text-sm font-light">$</span>72.00
            <svg class="w-6 h-6 text-gray-800 absolute right-3 top-0" aria-hidden="true" fill="currentColor"
                viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M10.75 4.75a.75.75 0 00-1.5 0v4.5h-4.5a.75.75 0 000 1.5h4.5v4.5a.75.75 0 001.5 0v-4.5h4.5a.75.75 0 000-1.5h-4.5v-4.5z">
                </path>
            </svg>
        </p>

    </div>
</template>

<script>
import customImage from '../assets/images/istockphoto-1349960077-612x612.jpg'
export default {
    data() {
        return {
            image: customImage,
        };
    }
};
</script>
