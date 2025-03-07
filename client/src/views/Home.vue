<script setup lang="ts">
import { onMounted, ref } from 'vue';
import ProjectCard from '../components/ProjectCard.vue';
import Background from '../components/Background.vue';
import CommUnity from '../assets/images/CommUnity.jpg';
import BetterCalendar from '../assets/images/Better-Calendar.png';
import FitnessTracker from '../assets/images/Fitness-Tracker.png';
import ComputationOptimizer from '../assets/images/Computation-Optimizer.png';


const projects = ref([
    {
        title: 'Better Calendar',
        description: 'Chrome Extension for intelligent event management with location-based reminders and route optimization',
        imageUrl: BetterCalendar,
        githubUrl: 'https://github.com/Youssup/BetterCalendar',
        features: [
            'Automated event reminders based on location',
            'Real-time route optimization with traffic',
            'AWS Lambda-powered 5-minute interval checks',
            'Flexible location override settings',
            'Google Calendar & Maps API integration'
        ],
        technologies: [
            {
                name: 'React',
                badgeUrl: 'https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB',
                url: 'https://reactjs.org/'
            },
            {
                name: 'Flask',
                badgeUrl: 'https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white',
                url: 'https://flask.palletsprojects.com/'
            },
            {
                name: 'Python',
                badgeUrl: 'https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white',
                url: 'https://www.python.org/'
            },
            {
                name: 'JavaScript',
                badgeUrl: 'https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black',
                url: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript'
            },
            {
                name: 'Tailwind CSS',
                badgeUrl: 'https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white',
                url: 'https://tailwindcss.com/'
            },
            {
                name: 'Google Cloud',
                badgeUrl: 'https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white',
                url: 'https://cloud.google.com/'
            },
            {
                name: 'AWS',
                badgeUrl: 'https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white',
                url: 'https://aws.amazon.com/'
            }
        ]
    },
    {
        title: 'CommUnity',
        description: 'Full-stack community platform enabling local engagement and resource sharing with real-time updates',
        imageUrl: CommUnity,
        features: [
            'Real-time community event tracking',
            'Resource sharing marketplace'
        ],
        demoUrl: 'https://hackrpi-1.onrender.com/',
        githubUrl: 'https://github.com/Youssup/CommUnity',
        technologies: [
            {
                name: 'Vue.js',
                badgeUrl: 'https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white',
                url: 'https://vuejs.org/'
            },
            {
                name: 'Express.js',
                badgeUrl: 'https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white',
                url: 'https://expressjs.com/'
            },
            {
                name: 'Node.js',
                badgeUrl: 'https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white',
                url: 'https://nodejs.org/'
            },
            {
                name: 'MongoDB',
                badgeUrl: 'https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white',
                url: 'https://www.mongodb.com/'
            },
            {
                name: 'TypeScript',
                badgeUrl: 'https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white',
                url: 'https://www.typescriptlang.org/'
            },
            {
                name: 'Tailwind CSS',
                badgeUrl: 'https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white',
                url: 'https://tailwindcss.com/'
            }
        ]
    },
    {
        title: 'Fitness Tracker',
        description: 'Comprehensive fitness tracking application with ML-powered workout recommendations and progress analytics',
        imageUrl: FitnessTracker,
        githubUrl: 'https://github.com/Youssup/Fitness-Website',
        features: [
            'Progress tracking and analytics',
            'Social workout sharing',
            'Local login and data storage',
            'Admin dashboard for user management'
        ],
        demoUrl: 'https://fitness-website-9h3r.onrender.com/',
        technologies: [
            {
                name: 'Vue.js',
                badgeUrl: 'https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white',
                url: 'https://vuejs.org/'
            },
            {
                name: 'Express.js',
                badgeUrl: 'https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white',
                url: 'https://expressjs.com/'
            },
            {
                name: 'Node.js',
                badgeUrl: 'https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white',
                url: 'https://nodejs.org/'
            },
            {
                name: 'TypeScript',
                badgeUrl: 'https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white',
                url: 'https://www.typescriptlang.org/'
            },
            {
                name: 'Bulma',
                badgeUrl: 'https://img.shields.io/badge/Bulma-00D1B2?style=for-the-badge&logo=bulma&logoColor=white',
                url: 'https://bulma.io/'
            }
        ]
    },
    {
        title: 'Computation Optimizer',
        description: 'High-performance computing solution that optimizes computational workflows and resource allocation',
        imageUrl: ComputationOptimizer,
        features: [
            'Multi-threading and dynamic programming',
            '90% increase in computational efficiency',
            'Resource allocation and optimization'
        ],
        githubUrl: 'https://github.com/Youssup/Computation-Optimizer',
        technologies: [
            {
                name: 'Java',
                badgeUrl: 'https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white',
                url: 'https://www.java.com/'
            },
            {
                name: 'JUnit',
                badgeUrl: 'https://img.shields.io/badge/JUnit-25A162?style=for-the-badge&logo=junit5&logoColor=white',
                url: 'https://junit.org/junit5/'
            },
            {
                name: 'Mockito',
                badgeUrl: 'https://img.shields.io/badge/Mockito-FF9900?style=for-the-badge&logo=mockito&logoColor=white',
                url: 'https://site.mockito.org/'
            },
            {
                name: 'gRPC',
                badgeUrl: 'https://img.shields.io/badge/gRPC-4285F4?style=for-the-badge&logo=grpc&logoColor=white',
                url: 'https://grpc.io/'
            },
            {
                name: 'Gradle',
                badgeUrl: 'https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white',
                url: 'https://gradle.org/'
            }
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
        <section id="home" class="container mx-auto min-h-screen flex items-center justify-center">
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
        </section>
    </Background>
    <div class="absolute bottom-0 left-0 right-0 w-full">
                <svg class="w-full h-32" preserveAspectRatio="none" viewBox="0 0 100 100" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <path d="M0 100V30C25 -10 75 -10 100 30V100H0Z" fill="url(#gradient)" />
                    <defs>
                        <linearGradient id="gradient" x1="50" y1="0" x2="50" y2="100" gradientUnits="userSpaceOnUse">
                            <stop offset="0%" stop-color="white" />
                            <stop offset="100%" stop-color="#E5E7EB" /> <!-- This is the Tailwind gray-200 color -->
                        </linearGradient>
                    </defs>
                </svg>
            </div>
    <div class="bg-gray-200 pb-28">
        <!-- Experience Section -->


        <div id="projects" class="max-w-7xl mx-auto flex flex-col gap-8 pt-4">
            <!-- Projects Section -->
            <div class="w-full mt-4">
                <h2 class="text-4xl font-bold mb-8 slide-in-element">Featured Projects</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
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