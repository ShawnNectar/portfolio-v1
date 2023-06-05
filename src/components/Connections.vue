<template>
    <div class="text-lg md:text-2xl text-blue-200 font-mono pt-10">
        <h1 class="text-green-600 py-2 md:py-5">// Connections </h1>
        <div>
            <h1 class="pb-2">
                <span class="text-orange-500">let </span>github = String::<span style="color: #50a8e4;">from</span>(
                <span style="color: #e70d0d;">"<a style="text-decoration: underline" href="https://github.com/ShawnNectar" target=”_blank”>github</a>"</span>);
            </h1>
            <h1 class="pt-6 pb-2">
                <span class="text-orange-500">let </span>email = String::<span style="color: #50a8e4;">from</span>(
                <span style="color: #e70d0d; cursor: pointer;" @click="copyText('shawnnectar@protonmail.com', 'showCopiedEmail')" ref="emailRef">"shawnnectar@protonmail.com"</span>);
                <span v-if="showCopiedEmail" class="text-green-500 ml-2">(Copied!)</span>
            </h1>
            <h1 class="pb-2">
                <span class="text-orange-500">let </span>discord = String::<span style="color: #50a8e4;">from</span>(
                <span style="color: #e70d0d; cursor: pointer;" @click="copyText('ShawnNectar#8155', 'showCopiedDiscord')" ref="discordRef">"ShawnNectar#8155"</span>);
                <span v-if="showCopiedDiscord" class="text-green-500 ml-2">(Copied!)</span>
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
