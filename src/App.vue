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
            <div class="grid lg:grid-cols-2 md:grid-cols-1 sm:grid-cols-1">
                <StuffIDo />
                <AboutMe />
            </div>

            <WorkInterests />


            <Connections />
            <Brazil />
        </div>
    </div>
</template>






