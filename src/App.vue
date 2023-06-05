<script setup>
import './index.css'
import StuffIDo from "@/components/StuffIDo.vue";
import AboutMe from "@/components/AboutMe.vue";
import WorkInterests from "@/components/WorkInterests.vue";
import Connections from "@/components/Connections.vue";
import Brazil from "@/components/Brazil.vue";
</script>

<template>
    <div class="lg:px-10 md:px-10 sm:px-0 pt-6">
        <div class="lg:px-0 md:px-10 sm:px-10">
            <h1 class="text-5xl font-semibold pb-5 text-amber-200">🤗 Hey, I'm Shawn!</h1>
            <div class="lg:flex md:block sm:block">
                <div class="lg:w-1/2 md:w-full sm:w-full">
                    <StuffIDo />
                </div>
                <div class="lg:w-1/2 md:w-full sm:w-full">
                    <AboutMe />
                </div>
            </div>
            <WorkInterests />
            <Connections />
            <Brazil />
        </div>
    </div>
</template>







