<template>
    <div>
        <NuxtPage />
        <div :class="{
            'fixed   translate-y-full transition-transform duration-500 ease-in-out': isScrolled,
            'transform bottom-0': !isScrolled
        }"
            class=" fixed flex justify-around items-start pt-3 bottom-0 left-0 right-0 m-auto rounded-[20px] w-11/12 h-16 bg-slate-800 transition-all duration-1000 ease-in-out">
            <svg class="w-6 h-6 text-white" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path clip-rule="evenodd"
                    d="M9.293 2.293a1 1 0 011.414 0l7 7A1 1 0 0117 11h-1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-3a1 1 0 00-1-1H9a1 1 0 00-1 1v3a1 1 0 01-1 1H5a1 1 0 01-1-1v-6H3a1 1 0 01-.707-1.707l7-7z"
                    fill-rule="evenodd"></path>
            </svg>
            <svg class="w-6 h-6 text-white" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M9.653 16.915l-.005-.003-.019-.01a20.759 20.759 0 01-1.162-.682 22.045 22.045 0 01-2.582-1.9C4.045 12.733 2 10.352 2 7.5a4.5 4.5 0 018-2.828A4.5 4.5 0 0118 7.5c0 2.852-2.044 5.233-3.885 6.82a22.049 22.049 0 01-3.744 2.582l-.019.01-.005.003h-.002a.739.739 0 01-.69.001l-.002-.001z">
                </path>
            </svg>
            <svg class="w-6 h-6 text-white" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path clip-rule="evenodd"
                    d="M6 5v1H4.667a1.75 1.75 0 00-1.743 1.598l-.826 9.5A1.75 1.75 0 003.84 19H16.16a1.75 1.75 0 001.743-1.902l-.826-9.5A1.75 1.75 0 0015.333 6H14V5a4 4 0 00-8 0zm4-2.5A2.5 2.5 0 007.5 5v1h5V5A2.5 2.5 0 0010 2.5zM7.5 10a2.5 2.5 0 005 0V8.75a.75.75 0 011.5 0V10a4 4 0 01-8 0V8.75a.75.75 0 011.5 0V10z"
                    fill-rule="evenodd"></path>
            </svg>
            <svg class="w-6 h-6 text-white" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M10 8a3 3 0 100-6 3 3 0 000 6zM3.465 14.493a1.23 1.23 0 00.41 1.412A9.957 9.957 0 0010 18c2.31 0 4.438-.784 6.131-2.1.43-.333.604-.903.408-1.41a7.002 7.002 0 00-13.074.003z">
                </path>
            </svg>
        </div>
        <div class="fixed bottom-0 h-9 w-full inline-block"  @click="slideUp" >
            <div :class="{ 'color-on-scroll': isScrolled }"
                class="w-[130px] rounded-lg  h-1 bg-white fixed bottom-3 m-auto  left-0 right-0"></div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isScrolled: false,
        };
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeDestroy() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll() {
            this.isScrolled = window.pageYOffset > 10;
        },
        slideUp() {
            this.isScrolled = false;
        },
    },
};


</script>
<style scoped>
.color-on-scroll {
    @apply bg-slate-800 transition-transform duration-1000
}
</style>

