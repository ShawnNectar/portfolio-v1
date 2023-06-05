<template>
    <div class="text-lg md:text-2xl text-blue-200 font-mono">
        <h1 class="text-green-600 py-2 md:py-5">// Connections</h1>
        <p class="pb-2">
            <span class="text-teal-600">let</span> connections = {
            <span class="text-teal-600">twitter</span>: <span style="color: #e70d0d;">"@shawn_dev"</span>,
            <span class="text-teal-600">github</span>: <span style="color: #e70d0d;">"shawn-dev"</span>,
            <span class="text-teal-600">linkedin</span>: <span style="color: #e70d0d;">"shawn-dev"</span>
            };
        </p>
        <p>
            <span class="text-teal-600">console.log</span>(<span class="text-teal-600">connections</span>);
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showCopiedEmail: false,
            showCopiedDiscord: false,
        };
    },
    methods: {
        copyText(text, flagName) {
            const el = document.createElement('textarea');
            el.value = text;
            document.body.appendChild(el);
            el.select();
            document.execCommand('copy');
            document.body.removeChild(el);

            this[flagName] = true;
            setTimeout(() => {
                this[flagName] = false;
            }, 1500);
        },
    },
};
</script>

<style scoped>
.text-green-500 {
    transition: opacity 1.5s;
}
</style>