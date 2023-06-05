<script setup>
import './index.css'
import StuffIDo from "@/components/StuffIDo.vue";
import AboutMe from "@/components/AboutMe.vue";
import WorkInterests from "@/components/WorkInterests.vue";
import Connections from "@/components/Connections.vue";
import Brazil from "@/components/Brazil.vue";
</script>

<template>
    <div class="px-10 pt-6">
        <div class="px-0 md:px-10">
            <h1 class="text-5xl font-semibold pb-5 text-amber-200">🤗 Hey, I'm Shawn!</h1>
            <div class="md:flex md:flex-wrap">
                <div class="md:w-1/2">
                    <StuffIDo />
                </div>
                <div class="md:w-1/2">
                    <AboutMe />
                </div>
            </div>

            <WorkInterests />

            <Connections />
            <Brazil />
        </div>
    </div>
</template>








