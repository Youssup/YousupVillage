<script setup>
import { onMounted, ref } from 'vue';
import ProjectCard from '../components/ProjectCard.vue';
import image from '../assets/images/CommUnity.jpg'
import Background from '../components/Background.vue';
const projects = ref([
    {
        title: 'Better Calendar',
        description: 'Chrome Extension for intelligent event management with location-based reminders and route optimization',
        imageUrl: '../assets/images/better-calendar.png',
        features: [
            'Automated event reminders based on location',
            'Real-time route optimization with traffic',
            'AWS Lambda-powered 5-minute interval checks',
            'Flexible location override settings',
            'Google Calendar & Maps API integration'
        ],
        technologies: [
            { name: 'React', class: 'bg-blue-100 text-blue-700' },
            { name: 'Flask', class: 'bg-green-100 text-green-700' },
            { name: 'Python', class: 'bg-yellow-100 text-yellow-700' },
            { name: 'AWS', class: 'bg-orange-100 text-orange-700' },
            { name: 'Google Cloud', class: 'bg-purple-100 text-purple-700' },
            { name: 'Tailwind', class: 'bg-cyan-100 text-cyan-700' }
        ]
    },
    {
        title: 'CommUnity',
        description: 'Full-stack community platform enabling local engagement and resource sharing with real-time updates',
        imageUrl: image,
        features: [
            'Real-time community event tracking',
            'Resource sharing marketplace',
            'User authentication and profiles',
            'Interactive community maps',
            'Event planning and RSVP system'
        ],
        technologies: [
            { name: 'React', class: 'bg-blue-100 text-blue-700' },
            { name: 'Node.js', class: 'bg-green-100 text-green-700' },
            { name: 'MongoDB', class: 'bg-purple-100 text-purple-700' },
            { name: '', class: 'bg-gray-100 text-gray-700' },
            { name: '', class: 'bg-red-100 text-red-700' },
            { name: '', class: 'bg-yellow-100 text-yellow-700' }
        ]
    },
    {
        title: 'Fitness Tracker',
        description: 'Comprehensive fitness tracking application with ML-powered workout recommendations and progress analytics',
        imageUrl: '',
        features: [
            'Custom workout plan generation',
            'Progress tracking and analytics',
            'Nutrition logging and analysis',
            'Machine learning recommendations',
            'Social workout sharing'
        ],
        technologies: [
            { name: '', class: 'bg-blue-100 text-blue-700' },
            { name: '', class: 'bg-green-100 text-green-700' },
            { name: '', class: 'bg-purple-100 text-purple-700' },
            { name: '', class: 'bg-cyan-100 text-cyan-700' },
            { name: '', class: 'bg-orange-100 text-orange-700' },
            { name: '', class: 'bg-indigo-100 text-indigo-700' }
        ]
    },
    {
        title: 'Computation Optimizer',
        description: 'High-performance computing solution that optimizes computational workflows and resource allocation',
        imageUrl: '',
        features: [
            'Parallel processing optimization',
            'Resource allocation algorithms',
            'Performance monitoring dashboard',
            'Automated workflow scheduling',
            'Load balancing system'
        ],
        technologies: [
            { name: '', class: 'bg-blue-100 text-blue-700' },
            { name: '', class: 'bg-green-100 text-green-700' },
            { name: '', class: 'bg-yellow-100 text-yellow-700' },
            { name: '', class: 'bg-cyan-100 text-cyan-700' },
            { name: '', class: 'bg-purple-100 text-purple-700' },
            { name: '', class: 'bg-orange-100 text-orange-700' }
        ]
    }
]);

onMounted(() => {
    if (window.customElements && !customElements.get("animated-icons")) {
        const script = document.createElement("script");
        script.src = "https://animatedicons.co/scripts/embed-animated-icons.js";
        document.body.appendChild(script);
    }
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
    <Background>
        <!-- Header -->
        <section class="container mx-auto min-h-screen flex items-center justify-center">
            <div class="w-full max-w-4xl mx-auto flex flex-col md:flex-row items-center justify-center gap-8 md:gap-12">
                <!-- Profile Picture -->
                <div class="w-72 md:w-80 lg:w-1/2 xxl:w-8/12 flex-shrink-0 flex items-center justify-center">
                    <div class="w-full aspect-square rounded-full ring ring-neutral-400 overflow-hidden">
                        <img src="../assets/images/profile.jpg" alt="Profile" class="w-full h-full object-cover" />
                    </div>
                </div>
                <!-- Text Content -->
                <div class="flex-1 flex flex-col items-center text-center">
                    <h1 class="text-2xl md:text-3xl mb-2">Yoosup Song</h1>
                    <h2 class="text-2xl md:text-3xl font-bold mb-4">Backend Software Engineer</h2>
                    <p class="text-gray-500">
                        <span>
                            <img src="../assets/icons/location-pin.svg" alt=""
                                class="w-4 h-4 inline-block fill-gray-500" />
                        </span>
                        Based in the U.S.
                    </p>
                    <!-- Social Links -->
                    <div class="flex flex-row justify-center gap-4 mt-8">
                        <!-- GitHub Button -->
                        <a href="https://github.com/Youssup" target="_blank" rel="noopener noreferrer">
                            <button class="learn-more">
                                <span class="circle" aria-hidden="true">
                                    <span class="icon arrow"></span>
                                </span>
                                <span class="button-text">Github</span>
                            </button>
                        </a>
                        <!-- LinkedIn Button -->
                        <a href="https://www.linkedin.com/in/yousupsong/" target="_blank" rel="noopener noreferrer">
                            <button class="learn-more">
                                <span class="circle" aria-hidden="true">
                                    <span class="icon arrow"></span>
                                </span>
                                <span class="button-text">LinkedIn</span>
                            </button>
                        </a>
                    </div>
                </div>
            </div>
            <div class="absolute bottom-0 left-0 right-0 w-full">
        <svg class="w-full h-32" preserveAspectRatio="none" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 100V30C25 -10 75 -10 100 30V100H0Z" fill="url(#gradient)"/>
            <defs>
                <linearGradient id="gradient" x1="50" y1="0" x2="50" y2="100" gradientUnits="userSpaceOnUse">
                    <stop offset="0%" stop-color="white"/>
                    <stop offset="100%" stop-color="#E5E7EB"/> <!-- This is the Tailwind gray-200 color -->
                </linearGradient>
            </defs>
        </svg>
    </div>
        </section>
    </Background>
    <div class="bg-gray-200">
        <div class="max-w-7xl mx-auto flex flex-col gap-8 pt-4">
            <!-- Projects Section -->
            <div id="projects" class="w-full mt-4">
                <h2 class="text-4xl font-bold mb-8 slide-in-element">Featured Projects</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
                </div>
            </div>

            <!-- Experience Section -->
            <div id="experience" class="w-full mt-4 slide-in-element">
                <h2 class="text-4xl font-bold mb-8">Experience</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <!-- Experience cards with slide-in-element class -->
                    <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                        <span class="text-sm text-neutral-500">Sep 2024 - Present</span>
                        <h3 class="text-xl font-bold mt-2 mb-3">Private Tutoring</h3>
                        <p class="text-neutral-600 group-hover:hidden">Providing personalized support and mentoring to
                            students.</p>
                        <p class="text-neutral-600 hidden group-hover:block">• Increased student grades by average of
                            15%<br>• Specialized in Python and web development<br>• Mentored 20+ students</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                        <span class="text-sm text-neutral-500">May 2024 - Present</span>
                        <h3 class="text-xl font-bold mt-2 mb-3">Support Engineer</h3>
                        <p class="text-neutral-600 group-hover:hidden">Technical assistance at Agile InfoTech.</p>
                        <p class="text-neutral-600 hidden group-hover:block">• Resolved 500+ technical tickets<br>•
                            Maintained 98% customer satisfaction<br>• Implemented new support workflow</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm hover-lift group">
                        <span class="text-sm text-neutral-500">May 2024 - Nov 2024</span>
                        <h3 class="text-xl font-bold mt-2 mb-3">Freelance Web Developer</h3>
                        <p class="text-neutral-600 group-hover:hidden">Designing and developing responsive websites.</p>
                        <p class="text-neutral-600 hidden group-hover:block">• Completed 15+ client projects<br>•
                            Specialized in Vue.js and React<br>• 100% client satisfaction rate</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
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
    background: #374151;
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
    color: #374151;
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
</style>