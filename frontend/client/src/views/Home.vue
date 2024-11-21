<script setup lang="ts">
import { onMounted } from 'vue';

onMounted(() => {
    const elements = document.querySelectorAll('.slide-in-element');
    const observer = new IntersectionObserver((entries, observer) => {
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
    elements.forEach((element) => observer.observe(element));
});
</script>

<template>
    <!-- Header -->
    <section id="header" class="puff-in-center container mx-auto min-h-screen flex flex-col justify-center items-center text-center">
    <h1 class="lg:self-start text-3xl md:text-5xl font-bold lg:ml-4 text-center ">Software</h1>
    <h1 class="lg:self-start text-3xl md:text-5xl lg:ml-24 font-bold text-center ">Engineer</h1>
    <div class="hero-content flex flex-col gap-10 sm:flex-row items-center sm:items-start text-center sm:text-left">
        <!-- Profile Picture -->
        <div class="avatar sm:w-3/6 mb-6 sm:mb-0">
            <div class="rounded-full border-2 border-neutral-400">
                <img src="../assets/images/download.jpg" alt="Profile" />
            </div>
        </div>

        <!-- Links -->
        <div class="my-auto flex flex-col items-center sm:items-start text-center sm:text-left">
            <div>
                <h1 class="text-2xl mb-4 sm:mb-6 text-center">Hello!</h1>
                <h1 class="intro hidden sm:block visible text-4xl font-bold">My name is Yoosup Song</h1>
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

    <!-- Experience -->
    <section id="experience">
        <h1 class="ml-8 text-6xl md:text-8xl md:ml-20 font-bold text-gray-400 slide-in-element">Experience</h1>
        <div
            class="mx-auto max-w-7xl px-8 md:px-12 lg:px-32 my-10 divide-y prose text-gray-500 prose-sm prose-headings:font-normal prose-headings:text-xl space-y-10 text-black text-sm">
            <div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-32 slide-in-element">
                <div>
                    <div class="lg:sticky lg:pb-16 top-0">
                        <div class="pt-8">
                            <p>Sep 2024 - Present</p>
                            <p>(3 months)</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-2 pt-8">
                    <div class="flex-shrink-0">
                        <div class="mx-auto">
                            <p class="text-4xl my-2 tracking-tighter font-semibold text-gray-700 text-balance">Private
                                Tutoring</p>
                            <p class="line-clamp-4">As a freelance tutor, I provide personalized support to students,
                                helping them with various academic subjects. My focus includes student development,
                                mentoring, and offering guidance in both technical and non-technical areas. I adapt my
                                teaching style to meet individual needs, ensuring effective learning outcomes.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-32 slide-in-element">
                <div>
                    <div class="lg:sticky lg:pb-16 top-0">
                        <div class="pt-8">
                            <p>May 2024 - Present</p>
                            <p>(7 months)</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-2 pt-8">
                    <div class="flex-shrink-0">
                        <div class="mx-auto ">
                            <p class="text-4xl my-2 tracking-tighter font-semibold text-gray-700 text-balance">
                                Support Engineer at Agile InfoTech</p>
                            <p class="line-clamp-4">In my current role as a part-time support engineer, I provide
                                technical assistance to clients, helping troubleshoot issues related to computer
                                hardware and software. I communicate effectively with customers to ensure their needs
                                are addressed and maintain strong technical support across the company's service
                                offerings.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-32 slide-in-element">
                <div>
                    <div class="lg:sticky lg:pb-16 top-0">
                        <div class="pt-8">
                            <p>May 2024 - Nov 2024</p>
                            <p>(7 months)</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-2 pt-8">
                    <div class="flex-shrink-0">
                        <div class="mx-auto ">
                            <p class="text-4xl my-2 tracking-tighter font-semibold text-gray-700 text-balance">
                                Freelance Web Developer</p>
                            <p class="line-clamp-4">As a freelance web developer, I design, develop, and deploy
                                responsive websites tailored to meet client needs. I work closely with clients to
                                understand their objectives, ensuring the final product aligns with their vision. My
                                work involves utilizing modern web technologies to create engaging and functional
                                websites.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-32 slide-in-element">
                <div>
                    <div class="lg:sticky lg:pb-16 top-0">
                        <div class="pt-8">
                            <p>August 2022 - Present</p>
                            <p>(2 years 4 months)</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-2 pt-8">
                    <div class="flex-shrink-0">
                        <div class="mx-auto ">
                            <p class="text-4xl my-2 tracking-tighter font-semibold text-gray-700 text-balance">
                                President of Eleet Coders </p>
                            <p class="line-clamp-4">As President, I oversee the operations of Eleet Coders, organizing
                                events, workshops, and networking opportunities for students pursuing careers in
                                computer science. My role involves fostering a collaborative learning environment,
                                ensuring members have the resources needed for professional growth, and representing the
                                club in university-wide initiatives.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-32 slide-in-element">
                <div>
                    <div class="lg:sticky lg:pb-16 top-0">
                        <div class="pt-8">
                            <p>Sep 2023 - Oct 2024</p>
                            <p>(1 year 2 months)</p>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-2 pt-8">
                    <div class="flex-shrink-0">
                        <div class="mx-auto ">
                            <p class="text-4xl my-2 tracking-tighter font-semibold text-gray-700 text-balance">
                                Sales Associate at Club Monaco</p>
                            <p class="line-clamp-4">As a Sales Associate at Club Monaco, I provided excellent customer
                                service, assisting clients with their purchases and ensuring a positive in-store
                                experience. My responsibilities included maintaining store presentation and supporting
                                the sales team in meeting performance goals.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
.custom-heading-left {
    text-align: left !important; /* Override text-center for left alignment */
    margin-left: 0 !important;   /* Ensure no margin on the left */
}

.custom-heading-left {
    text-align: left !important; /* Override text-center for larger screens */
    margin-left: 24px !important; /* Custom margin for md and up screens */
}

html {
    scroll-behavior: smooth;
}

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