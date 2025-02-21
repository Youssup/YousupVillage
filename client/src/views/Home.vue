<script setup lang="ts">
import { onMounted, ref } from 'vue';

const stats = ref({
    commits: '500+',
    repositories: '25+',
    contributions: '365+',
    connections: '200+'
});

onMounted(() => {
    const elements = document.querySelectorAll('.fade-in');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('fade-in-visible');
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.1 });
    
    elements.forEach(element => observer.observe(element));
});
</script>

<template>
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white/80 backdrop-blur-sm z-50 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
            <h1 class="text-xl font-bold">YS</h1>
            <div class="flex gap-6">
                <a href="#experience" class="hover-jiggle">Experience</a>
                <a href="#projects" class="hover-jiggle">Projects</a>
                <a href="#contact" class="hover-jiggle">Contact</a>
            </div>
        </div>
    </nav>

    <main class="min-h-screen bg-neutral-50 p-4 md:p-8 pt-20">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 max-w-7xl mx-auto">
            <!-- Profile Card -->
            <div class="col-span-1 md:col-span-2 lg:col-span-2 bg-white rounded-3xl p-8 shadow-sm fade-in hover-lift">
                <div class="flex flex-col md:flex-row items-center gap-8">
                    <div class="w-48 h-48 md:w-56 md:h-56 overflow-hidden rounded-full ring-4 ring-neutral-100 hover-rotate">
                        <img src="../assets/images/profile.jpg" alt="Profile" class="w-full h-full object-cover" />
                    </div>
                    <div class="flex flex-col items-center md:items-start">
                        <h1 class="text-4xl font-bold mb-4">Yoosup Song</h1>
                        <h2 class="text-2xl text-neutral-600 mb-6">Software Engineer</h2>
                        <p class="text-neutral-600 mb-6">Passionate about creating intuitive web experiences and solving complex problems.</p>
                        <div class="flex gap-4">
                            <a href="https://github.com/Youssup" target="_blank" 
                               class="px-6 py-2 bg-neutral-900 text-white rounded-full hover:bg-neutral-800 transition-colors hover-jiggle">
                                GitHub
                            </a>
                            <a href="https://www.linkedin.com/in/yousupsong/" target="_blank"
                               class="px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition-colors hover-jiggle">
                                LinkedIn
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Stats Card -->
            <div class="bg-gradient-to-br from-purple-500 to-blue-500 rounded-3xl p-8 text-white fade-in hover-lift">
                <div class="grid grid-cols-2 gap-4">
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
            <div id="projects" class="col-span-1 md:col-span-2 lg:col-span-3 mt-4">
                <h2 class="text-4xl font-bold mb-8 text-neutral-800">Featured Projects</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
                        <div class="relative overflow-hidden rounded-xl mb-4">
                            <img src="" alt="Project 1" class="w-full h-48 object-cover" />
                            <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                                <p class="text-white text-center p-4">A real-time collaborative coding platform built with Vue.js and WebSocket</p>
                            </div>
                        </div>
                        <h3 class="text-xl font-bold">CodeCollab</h3>
                        <p class="text-neutral-600 mt-2">Vue.js, Socket.io, Express</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
                        <div class="relative overflow-hidden rounded-xl mb-4">
                            <img src=" " alt="Project 2" class="w-full h-48 object-cover" />
                            <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
                                <p class="text-white text-center p-4">AI-powered task management system with natural language processing</p>
                            </div>
                        </div>
                        <h3 class="text-xl font-bold">TaskAI</h3>
                        <p class="text-neutral-600 mt-2">Python, FastAPI, React</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
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
            <div id="experience" class="col-span-1 md:col-span-2 lg:col-span-3 mt-4">
                <h2 class="text-4xl font-bold mb-8 text-neutral-800">Experience</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <!-- Experience cards with hover context -->
                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
                        <span class="text-sm text-neutral-500">Sep 2024 - Present</span>
                        <h3 class="text-xl font-bold mt-2 mb-3">Private Tutoring</h3>
                        <p class="text-neutral-600 group-hover:hidden">Providing personalized support and mentoring to students.</p>
                        <p class="text-neutral-600 hidden group-hover:block">• Increased student grades by average of 15%<br>• Specialized in Python and web development<br>• Mentored 20+ students</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
                        <span class="text-sm text-neutral-500">May 2024 - Present</span>
                        <h3 class="text-xl font-bold mt-2 mb-3">Support Engineer</h3>
                        <p class="text-neutral-600 group-hover:hidden">Technical assistance at Agile InfoTech.</p>
                        <p class="text-neutral-600 hidden group-hover:block">• Resolved 500+ technical tickets<br>• Maintained 98% customer satisfaction<br>• Implemented new support workflow</p>
                    </div>

                    <div class="bg-white rounded-3xl p-6 shadow-sm fade-in hover-lift group">
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
.fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in-visible {
    opacity: 1;
    transform: translateY(0);
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

.hover-rotate {
    transition: transform 0.3s ease;
}

.hover-rotate:hover {
    transform: rotate(5deg);
}

.hover-jiggle {
    display: inline-block;
    transition: transform 0.2s ease;
}

.hover-jiggle:hover {
    animation: jiggle 0.5s ease infinite;
}

@keyframes jiggle {
    0%, 100% { transform: rotate(0); }
    25% { transform: rotate(-3deg); }
    75% { transform: rotate(3deg); }
}

html {
    scroll-behavior: smooth;
}
</style>