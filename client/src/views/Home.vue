<script setup lang="ts">
import { onMounted, ref } from 'vue';

const stats = ref({
    commits: '500+',
    repositories: '25+',
    contributions: '365+',
    connections: '200+'
});

onMounted(() => {
    // Fade in observer
    const fadeElements = document.querySelectorAll('.fade-in');
    const fadeObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('fade-in-visible');
                fadeObserver.unobserve(entry.target);
            }
        });
    }, { threshold: 0.1 });
    
    fadeElements.forEach(element => fadeObserver.observe(element));

    // Slide in observer
    const slideElements = document.querySelectorAll('.slide-in-element');
    const slideObserver = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                if (!entry.target.classList.contains('animated')) {
                    entry.target.classList.add('slide-in-bottom');
                    entry.target.classList.add('animated');
                }
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.5 });
    slideElements.forEach((element) => slideObserver.observe(element));
});
</script>

<template>
<main id="home" class="puff-in-center min-h-screen bg-neutral-50 p-4 md:p-8">
    <div class="max-w-7xl mx-auto flex flex-col gap-8">
        <!-- Header -->
    <section class="container mx-auto min-h-screen flex flex-col justify-center items-center text-center">
        <h1 class="lg:self-start text-3xl md:text-5xl font-bold lg:ml-4 text-center ">Software</h1>
        <h1 class="lg:self-start text-3xl md:text-5xl lg:ml-24 font-bold text-center ">Engineer</h1>
        <div class="hero-content flex flex-col sm:flex-row items-center sm:items-start text-center sm:text-left">
            <!-- Profile Picture -->
            <div class="avatar mb-6">
                <div class="w-64 md:w-72 lg:w-96 xl:w-10/12 rounded-full ring ring-neutral-400">
                    <img src="../assets/images/profile.jpg" alt="Profile" />
                </div>
            </div>
            <!-- Links -->
            <div class="my-auto flex flex-col items-center sm:items-start text-center sm:text-left">
                <div>
                    <h1 class="text-2xl mb-4 sm:mb-6 text-center">Hello!</h1>
                    <h1 class="intro hidden sm:block visible text-4xl font-bold py-2">My name is Yoosup Song</h1>
                    <h1 class="intro text-4xl sm:hidden font-bold">My name is Yoosup</h1>
                </div>
                <div class="flex flex-col sm:flex-row sm:space-x-4 mt-6">
                    <!-- GitHub Button -->
                    <a href="https://github.com/Youssup" target="_blank">
                        <button class="learn-more mb-4 sm:mb-0">
                            <span class="circle" aria-hidden="true">
                                <span class="icon arrow"></span>
                            </span>
                            <span class="button-text">
                                GitHub
                            </span>
                        </button>
                    </a>
                    <!-- LinkedIn Button -->
                    <a href="https://www.linkedin.com/in/yousupsong/" target="_blank">
                        <button class="learn-more">
                            <span class="circle" aria-hidden="true">
                                <span class="icon arrow"></span>
                            </span>
                            <span class="button-text">
                                LinkedIn
                            </span>
                        </button>
                    </a>
                </div>
            </div>
        </div>
    </section>

        <!-- Stats Card - Full Width -->
        <div class="w-full bg-gradient-to-br from-gray-600 to-gray-900 rounded-3xl p-8 text-white fade-in hover-lift">
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
        <div class="text-center hover-pop">
            <h3 class="text-3xl font-bold">{{ stats.commits }}</h3>
            <p class="text-sm">Github Commits</p>
        </div>
        <div class="text-center hover-pop">
            <h3 class="text-3xl font-bold">{{ stats.repositories }}</h3>
            <p class="text-sm">Repositories</p>
        </div>
        <div class="text-center hover-pop">
            <h3 class="text-3xl font-bold">{{ stats.contributions }}</h3>
            <p class="text-sm">Contributions</p>
        </div>
        <div class="text-center hover-pop">
            <h3 class="text-3xl font-bold">{{ stats.connections }}</h3>
            <p class="text-sm">LinkedIn Connections</p>
        </div>
    </div>
</div>

        <!-- Projects Section -->
        <div id="projects" class="w-full mt-4 slide-in-element">
            <h2 class="text-4xl font-bold mb-8 text-neutral-800">Featured Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Project cards remain the same but with slide-in-element class -->
                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <div class="relative overflow-hidden rounded-xl mb-4">
                        <img src="" alt="Project 1" class="w-full h-48 object-cover" />
                        <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <p class="text-white text-center p-4">A real-time collaborative coding platform built with Vue.js and WebSocket</p>
                        </div>
                    </div>
                    <h3 class="text-xl font-bold">CodeCollab</h3>
                    <p class="text-neutral-600 mt-2">Vue.js, Socket.io, Express</p>
                </div>

                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <div class="relative overflow-hidden rounded-xl mb-4">
                        <img src=" " alt="Project 2" class="w-full h-48 object-cover" />
                        <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <p class="text-white text-center p-4">AI-powered task management system with natural language processing</p>
                        </div>
                    </div>
                    <h3 class="text-xl font-bold">TaskAI</h3>
                    <p class="text-neutral-600 mt-2">Python, FastAPI, React</p>
                </div>

                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <div class="relative overflow-hidden rounded-xl mb-4">
                        <img src="" alt="Project 3" class="w-full h-48 object-cover" />
                        <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                            <p class="text-white text-center p-4">E-commerce platform with real-time inventory management</p>
                        </div>
                    </div>
                    <h3 class="text-xl font-bold">ShopSync</h3>
                    <p class="text-neutral-600 mt-2">Next.js, MongoDB, Stripe</p>
                </div>
            </div>
        </div>

        <!-- Experience Section -->
        <div id="experience" class="w-full mt-4 slide-in-element">
            <h2 class="text-4xl font-bold mb-8 text-neutral-800">Experience</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <!-- Experience cards with slide-in-element class -->
                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <span class="text-sm text-neutral-500">Sep 2024 - Present</span>
                    <h3 class="text-xl font-bold mt-2 mb-3">Private Tutoring</h3>
                    <p class="text-neutral-600 group-hover:hidden">Providing personalized support and mentoring to students.</p>
                    <p class="text-neutral-600 hidden group-hover:block">• Increased student grades by average of 15%<br>• Specialized in Python and web development<br>• Mentored 20+ students</p>
                </div>

                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <span class="text-sm text-neutral-500">May 2024 - Present</span>
                    <h3 class="text-xl font-bold mt-2 mb-3">Support Engineer</h3>
                    <p class="text-neutral-600 group-hover:hidden">Technical assistance at Agile InfoTech.</p>
                    <p class="text-neutral-600 hidden group-hover:block">• Resolved 500+ technical tickets<br>• Maintained 98% customer satisfaction<br>• Implemented new support workflow</p>
                </div>

                <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                    <span class="text-sm text-neutral-500">May 2024 - Nov 2024</span>
                    <h3 class="text-xl font-bold mt-2 mb-3">Freelance Web Developer</h3>
                    <p class="text-neutral-600 group-hover:hidden">Designing and developing responsive websites.</p>
                    <p class="text-neutral-600 hidden group-hover:block">• Completed 15+ client projects<br>• Specialized in Vue.js and React<br>• 100% client satisfaction rate</p>
                </div>
            </div>
        </div>
    </div>
</main>
</template>

<style scoped>
/* Previous styles remain the same */
.fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in-visible {
    opacity: 1;
    transform: translateY(0);
}

/* Add new slide-in animation styles */
.slide-in-element {
    opacity: 0;
    transform: translateY(100px);
}

.slide-in-bottom {
    -webkit-animation: slide-in-bottom 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    animation: slide-in-bottom 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    opacity: 1;
    transform: translateY(0);
}

@keyframes slide-in-bottom {
    0% {
        transform: translateY(100px);
        opacity: 0;
    }
    100% {
        transform: translateY(0);
        opacity: 1;
    }
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

.hover-lift {
    transition: transform 0.3s ease;
}

.hover-lift:hover {
    transform: translateY(-5px);
}

.hover-pop {
    transition: transform 0.2s ease;
}

.hover-pop:hover {
    transform: scale(1.05);
}

.custom-heading-left {
    text-align: left !important;
    /* Override text-center for left alignment */
    margin-left: 0 !important;
    /* Ensure no margin on the left */
}

.custom-heading-left {
    text-align: left !important;
    /* Override text-center for larger screens */
    margin-left: 24px !important;
    /* Custom margin for md and up screens */
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