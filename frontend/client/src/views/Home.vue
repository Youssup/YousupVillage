<script setup lang="ts">

</script>

<script setup lang="ts">
</script>

<template>
    <!-- Header -->
    <div class="container mx-auto puff-in-center">
        <div class="hero-content flex flex-col gap-x-20 sm:flex-row items-center sm:items-start">
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