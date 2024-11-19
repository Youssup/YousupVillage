<script setup lang="ts">

</script>

<script setup lang="ts">
</script>

<template>
    <!-- Header -->
    <div class="container mx-auto puff-in-center">
        <div class="hero-content flex flex-col gap-x-10 sm:flex-row items-center sm:items-start">
            <!-- Profile Picture -->
            <div class="avatar w-40 sm:w-3/6 mb-6 sm:mb-0 brightness-90">
                <div class="rounded-full border-2 border-neutral-400">
                    <img src="../assets/icons/profile.jpg" alt="Profile" />
                </div>
            </div>

            <!-- Links -->
            <div class="flex flex-col items-center my-auto sm:items-start text-center sm:text-left">
                <div>
                    <h1 class="text-2xl mb-6 text-center">Hello!</h1>
                    <h1 class="intro text-4xl font-bold">My name is Yousup</h1>
                </div>
                <div class="flex flex-col sm:flex-row sm:space-x-4 mt-6">
                    <!-- GitHub Button -->
                    <button class="learn-more mb-4 sm:mb-0">
                        <span class="circle" aria-hidden="true">
                            <span class="icon arrow"></span>
                        </span>
                        <span class="button-text">
                            <a href="https://github.com/Youssup" target="_blank">GitHub</a>
                        </span>
                    </button>
                    <!-- LinkedIn Button -->
                    <button class="learn-more">
                        <span class="circle" aria-hidden="true">
                            <span class="icon arrow"></span>
                        </span>
                        <span class="button-text">
                            <a href="https://www.linkedin.com/in/yousupsong/" target="_blank">LinkedIn</a>
                        </span>
                    </button>
                </div>
            </div>
        </div>
    </div>
    <!-- Summary -->
    <section>
        <div class="px-8 py-24 mx-auto md:px-12 lg:px-32 max-w-screen-xl flex flex-col lg:h-svh justify-center">
            <div class="flex flex-col ">
                <div class="prose text-gray-500 prose-sm prose-headings:font-normal prose-headings:text-xl">
                    <div>
                        <h1>Simplified markup</h1>
                        <p class="text-balance">
                            See the code for this page to see how you can use Astro to simplify your markup.
                        </p>
                    </div>
                </div> <!-- Starts component -->
                <div class="mt-6 border-t pt-12">
                    <div class="grid grid-cols-1 gap-8 md:grid-cols-2 md:gap-24 items-center ">
                        <div> <span class="text-gray-600  uppercase text-xs font-medium "> Because why not </span>
                            <p class="text-4xl mt-8 tracking-tighter font-semibold text-gray-700 text-balance">
                                Innovative financial solutions for every situation </p>
                            <p class="text-sm  mt-4 text-gray-700 text-balance"> Discover a variety of tools, services,
                                and expert guidance tailored to your unique financial needs. </p>
                            <div
                                class="mt-6 text-xs font-medium grid grid-cols-1 sm:grid-cols-2 md:grid-cols-1 lg:grid-cols-2 gap-2 text-gray-950">
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        class="icon icon-tabler text-gray-700 size-4 icon-tabler-360"
                                        viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path
                                            d="M17 15.328c2.414 -.718 4 -1.94 4 -3.328c0 -2.21 -4.03 -4 -9 -4s-9 1.79 -9 4s4.03 4 9 4">
                                        </path>
                                        <path d="M9 13l3 3l-3 3"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Clear data visibility
                                    </span> </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        class="icon icon-tabler text-gray-700 size-4 icon-tabler-antenna-bars-3"
                                        viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M6 18l0 -3"></path>
                                        <path d="M10 18l0 -6"></path>
                                        <path d="M14 18l0 .01"></path>
                                        <path d="M18 18l0 .01"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Reduced external factors
                                    </span> </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        class="icon icon-tabler text-gray-700 size-4 icon-tabler-load-balancer"
                                        viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M12 13m-3 0a3 3 0 1 0 6 0a3 3 0 1 0 -6 0"></path>
                                        <path d="M12 20m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0"></path>
                                        <path d="M12 16v3"></path>
                                        <path d="M12 10v-7"></path>
                                        <path d="M9 6l3 -3l3 3"></path>
                                        <path d="M12 10v-7"></path>
                                        <path d="M9 6l3 -3l3 3"></path>
                                        <path d="M14.894 12.227l6.11 -2.224"></path>
                                        <path d="M17.159 8.21l3.845 1.793l-1.793 3.845"></path>
                                        <path d="M9.101 12.214l-6.075 -2.211"></path>
                                        <path d="M6.871 8.21l-3.845 1.793l1.793 3.845"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> enhanced stabilty </span>
                                </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        class="icon icon-tabler text-gray-700 size-4 icon-tabler-brand-speedtest"
                                        viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M5.636 19.364a9 9 0 1 1 12.728 0"></path>
                                        <path d="M16 9l-4 4"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> accelerated times </span>
                                </div>
                            </div>
                        </div>
                        <div class="h-full md:order-first"> <img
                                src="https://i.pinimg.com/564x/59/41/a0/5941a02c048f6226031a0487451c2651.jpg" alt="#_"
                                class=" bg-gray-200 shadow-box shadow-gray-500/30 overflow-hidden aspect-square  w-full h-full object-cover object-center">
                        </div>
                    </div>
                    <div class="grid grid-cols-1 gap-8 md:grid-cols-2 md:gap-24 items-center md:flex-row-reverse">
                        <div> <span class="text-gray-600  uppercase text-xs font-medium "> Just because we can </span>
                            <p class="text-4xl mt-8 tracking-tighter font-semibold text-gray-700 text-balance"> Tailored
                                financial solutions for any scenario </p>
                            <p class="text-sm  mt-4 text-gray-700 text-balance"> Discover a range of financial
                                instruments and personalized advice designed to meet your unique requirements. </p>
                            <div
                                class="mt-6 text-xs font-medium grid grid-cols-1 sm:grid-cols-2 md:grid-cols-1 lg:grid-cols-2 gap-2 text-gray-950">
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        xmlns="http://www.w3.org/2000/svg"
                                        class="icon icon-tabler icon-tabler-database text-gray-700 size-4"
                                        viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M12 6m-8 0a8 3 0 1 0 16 0a8 3 0 1 0 -16 0"></path>
                                        <path d="M4 6v6a8 3 0 0 0 16 0v-6"></path>
                                        <path d="M4 12v6a8 3 0 0 0 16 0v-6"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Transparent Data Access
                                    </span> </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        xmlns="http://www.w3.org/2000/svg"
                                        class="icon icon-tabler icon-tabler-building text-gray-700 size-4"
                                        viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M3 21l18 0"></path>
                                        <path d="M9 8l1 0"></path>
                                        <path d="M9 12l1 0"></path>
                                        <path d="M9 16l1 0"></path>
                                        <path d="M14 8l1 0"></path>
                                        <path d="M14 12l1 0"></path>
                                        <path d="M14 16l1 0"></path>
                                        <path d="M5 21v-16a2 2 0 0 1 2 -2h10a2 2 0 0 1 2 2v16"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Lowered Interference </span>
                                </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        xmlns="http://www.w3.org/2000/svg"
                                        class="icon icon-tabler icon-tabler-augmented-reality-2 text-gray-700 size-4"
                                        viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M10 21h-2a2 2 0 0 1 -2 -2v-14a2 2 0 0 1 2 -2h8a2 2 0 0 1 2 2v3.5">
                                        </path>
                                        <path d="M17 17l-4 -2.5l4 -2.5l4 2.5v4.5l-4 2.5z"></path>
                                        <path d="M13 14.5v4.5l4 2.5"></path>
                                        <path d="M17 17l4 -2.5"></path>
                                        <path d="M11 4h2"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Improved Reliability </span>
                                </div>
                                <div class="inline-flex items-center gap-2  text-xs text-gray-700"> <svg
                                        xmlns="http://www.w3.org/2000/svg"
                                        class="icon icon-tabler icon-tabler-time-duration-0 text-gray-700 size-4"
                                        viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none"
                                        stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M3 12v.01"></path>
                                        <path d="M21 12v.01"></path>
                                        <path d="M12 21v.01"></path>
                                        <path d="M12 3v.01"></path>
                                        <path d="M7.5 4.2v.01"></path>
                                        <path d="M16.5 4.2v.01"></path>
                                        <path d="M16.5 19.8v.01"></path>
                                        <path d="M7.5 19.8v.01"></path>
                                        <path d="M4.2 16.5v.01"></path>
                                        <path d="M19.8 16.5v.01"></path>
                                        <path d="M19.8 7.5v.01"></path>
                                        <path d="M4.2 7.5v.01"></path>
                                        <path d="M10 11v2a2 2 0 1 0 4 0v-2a2 2 0 1 0 -4 0z"></path>
                                    </svg> <span class="text-gray-950 font-medium text-sm"> Faster Processing Times
                                    </span> </div>
                            </div>
                        </div>
                        <div class="h-full "> <img
                                src="https://i.pinimg.com/564x/4e/a7/ff/4ea7ff230ad9f3bc1c30b1b6cbaccad3.jpg" alt="#_"
                                class=" bg-gray-200 shadow-box shadow-gray-500/30 overflow-hidden aspect-square  w-full h-full object-cover object-center">
                        </div>
                    </div>
                </div> <!-- Emds component -->
            </div>
        </div>
    </section>
</template>

<style>
.puff-in-center {
    -webkit-animation: puff-in-center .7s cubic-bezier(.47, 0.000, .745, .715) both;
    animation: puff-in-center .7s cubic-bezier(.47, 0.000, .745, .715) both
}

.intro {
    overflow: hidden;
    border-right: .15em solid gray;
    white-space: nowrap;
    margin: 0 auto;
    font-family: "Varela Round", sans-serif;
    font-weight: 400;
    font-style: normal;
    color: #333;
    animation:
        typing 3.5s steps(40, end),
        blink-caret .75s step-end infinite;
    animation-delay: .3s;
}

button {
    position: relative;
    display: inline-block;
    cursor: pointer;
    outline: none;
    border: 0;
    vertical-align: middle;
    text-decoration: none;
    background: transparent;
    padding: 0;
    font-size: inherit;
    font-family: inherit;
}

button.learn-more {
    width: 12rem;
    height: auto;
}

button.learn-more .circle {
    transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
    position: relative;
    display: block;
    margin: 0;
    width: 3rem;
    height: 3rem;
    background: #282936;
    border-radius: 1.625rem;
}

button.learn-more .circle .icon {
    transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    background: #fff;
}

button.learn-more .circle .icon.arrow {
    transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
    left: 0.625rem;
    width: 1.125rem;
    height: 0.125rem;
    background: none;
}

button.learn-more .circle .icon.arrow::before {
    position: absolute;
    content: "";
    top: -0.29rem;
    right: 0.0625rem;
    width: 0.625rem;
    height: 0.625rem;
    border-top: 0.125rem solid #fff;
    border-right: 0.125rem solid #fff;
    transform: rotate(45deg);
}

button.learn-more .button-text {
    transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    padding: 0.75rem 0;
    margin: 0 0 0 1.85rem;
    color: #282936;
    font-weight: 700;
    line-height: 1.6;
    text-align: center;
    text-transform: uppercase;
}

button:hover .circle {
    width: 100%;
}

button:hover .circle .icon.arrow {
    background: #fff;
    transform: translate(1rem, 0);
}

button:hover .button-text {
    color: #fff;
}

@-webkit-keyframes puff-in-center {
    0% {
        -webkit-transform: scale(2);
        transform: scale(2);
        -webkit-filter: blur(4px);
        filter: blur(4px);
        opacity: 0
    }

    100% {
        -webkit-transform: scale(1);
        transform: scale(1);
        -webkit-filter: blur(0);
        filter: blur(0);
        opacity: 1
    }
}

@keyframes puff-in-center {
    0% {
        -webkit-transform: scale(2);
        transform: scale(2);
        -webkit-filter: blur(4px);
        filter: blur(4px);
        opacity: 0
    }

    100% {
        -webkit-transform: scale(1);
        transform: scale(1);
        -webkit-filter: blur(0);
        filter: blur(0);
        opacity: 1
    }
}

@keyframes typing {
    from {
        width: 0
    }

    to {
        width: 100%
    }
}

@keyframes blink-caret {

    from,
    to {
        border-color: transparent
    }

    50% {
        border-color: gray;
    }
}
</style>