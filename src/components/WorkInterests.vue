<script setup>

</script>

<template>
    <div class="text-lg md:text-2xl text-blue-200 font-mono">
        <h1 class="text-green-600 py-2 md:py-5">// Work Interests</h1>
        <p class="pb-2">
            <span class="text-teal-600">const</span> workInterests = [
            <span style="color: #e70d0d;">"Artificial Intelligence",</span>
            <span style="color: #e70d0d;">"Machine Learning",</span>
            <span style="color: #e70d0d;">"Web Development",</span>
            <span style="color: #e70d0d;">"Data Science",</span>
            <span style="color: #e70d0d;">"Software Engineering"</span>
            ];
        </p>
        <p>
            <span class="text-teal-600">workInterests.forEach</span>(<span class="text-teal-600">(interest)</span> => <span class="text-teal-600">console.log</span>(<span class="text-teal-600">interest</span>));
        </p>
    </div>
</template>


<style scoped>

</style>