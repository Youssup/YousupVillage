<script setup lang="ts">
</script>

<template>
    <div>
        <div class="container mx-auto pt-20 puff-in-center">
            <div class="hero-content flex-col lg:flex-row">
                <div class="avatar w-3/6 brightness-90">
                    <div class="rounded-full border-2 border-neutral-400">
                        <img src="../components/icons/profile.jpg" />
                    </div>
                </div>
                <div>
                    <h1 class="intro text-5xl font-bold">Hello! My name is Yousup</h1>      
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.puff-in-center{-webkit-animation:puff-in-center .7s cubic-bezier(.47,0.000,.745,.715) both;animation:puff-in-center .7s cubic-bezier(.47,0.000,.745,.715) both}

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

@-webkit-keyframes puff-in-center{0%{-webkit-transform:scale(2);transform:scale(2);-webkit-filter:blur(4px);filter:blur(4px);opacity:0}100%{-webkit-transform:scale(1);transform:scale(1);-webkit-filter:blur(0);filter:blur(0);opacity:1}}@keyframes puff-in-center{0%{-webkit-transform:scale(2);transform:scale(2);-webkit-filter:blur(4px);filter:blur(4px);opacity:0}100%{-webkit-transform:scale(1);transform:scale(1);-webkit-filter:blur(0);filter:blur(0);opacity:1}}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: gray; }
}
</style>