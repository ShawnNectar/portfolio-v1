<template>
    <div class="font-mono text-2xl text-blue-200 pt-10 pb-5">
        <h1 class="text-2xl text-green-600 font-mono pb-2">// Connections</h1>
        <div>
            <h1 class="pt-6 pb-2">
                <span class="text-orange-500">let</span> github = String::<span style="color: #50a8e4;">from</span>(<span style="color: #e70d0d;">"<a style="text-decoration: underline" href="https://github.com/ShawnNectar" target="_blank">github</a>"</span>);
            </h1>
            <h1 class="pt-6 pb-2">
                <span class="text-orange-500">let</span> email = String::<span style="color: #e70d0d;">"<a style="text-decoration: underline" href="mailto:shawn@example.com">shawn@example.com</a>"</span>);
            </h1>
            <h1 class="pt-6 pb-2">
                <span class="text-orange-500">let</span> linkedin = String::<span style="color: #e70d0d;">"<a style="text-decoration: underline" href="https://linkedin.com/in/shawnnectar" target="_blank">linkedin</a>"</span>);
            </h1>
            <h1 class="pt-6 pb-2">
                <span class="text-orange-500">let</span> twitter = String::<span style="color: #e70d0d;">"<a style="text-decoration: underline" href="https://twitter.com/ShawnNectar" target="_blank">twitter</a>"</span>);
            </h1>
        </div>
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
