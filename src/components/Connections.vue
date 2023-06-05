<template>
    <div class="text-sm sm:text-3xl md:text-2xl text-blue-200 font-mono pt-10">
        <h1 class="text-green-600 py-2 md:py-5 ">// Connections </h1>
        <div>
            <h1 class="pb-2">
                <span class="text-orange-500">let </span>github = String::<span style="color: #50a8e4;">from</span>(<span style="color: #fc8140;">"<a style="text-decoration: underline" href="https://github.com/ShawnNectar" target=”_blank”>github</a>"</span>);
            </h1>

            <h2 class="pt-6 pb-2">
                <span class="text-orange-500">fn</span> <span class="text-amber-300">click_to_copy</span>() {
            </h2>
            <h2 class=" pb-2">
                <span class="text-orange-500">⠀let </span>email = <br class="md:hidden"/><span class="md:hidden">⠀</span>String::<span style="color: #50a8e4;">from</span>(<span style="color: #fc8140; cursor: pointer;" @click="copyText('\t\n'+'shawnnectar@pm.me', 'showCopiedEmail')" ref="emailRef">"shawnnectar@pm.me"</span>);
                <span v-if="showCopiedEmail" class="text-green-500 ml-2">(Copied!)</span>
            </h2>
            <h2 class="pb-2">
                <span class="text-orange-500">⠀let </span>discord = <br class="md:hidden"/><span class="md:hidden">⠀</span>String::<span style="color: #50a8e4;">from</span>(<span style="color: #fc8140; cursor: pointer;" @click="copyText('ShawnNectar#8155', 'showCopiedDiscord')" ref="discordRef">"ShawnNectar#8155"</span>);
                <span v-if="showCopiedDiscord" class="text-green-500 ml-2">(Copied!)</span> <br>}
            </h2>
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

@media (min-width: 768px) {
    .md\:hidden {
        display: none;
    }
}

</style>

