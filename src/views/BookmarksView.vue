<template>
    <!-- 复用 App.vue 提供的主容器，只添加垂直内边距 -->
    <div class="py-16">
        <h1 class="text-3xl font-bold mb-8 text-center">Bookmark Navigation</h1>
        <div v-for="group in bookmarkGroups" :key="group.title" class="mb-12">
            <h2 class="text-xl font-semibold mb-4 text-neutral-800">{{ group.title }}</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
                <a v-for="item in group.items" :key="item.name" :href="item.url" target="_blank" rel="noopener"
                    class="group block rounded-xl border border-neutral-200 bg-white p-4 shadow-sm hover:shadow-md transition hover:border-blue-400">
                    <div class="font-medium text-base mb-1 group-hover:text-blue-700">{{ item.name }}</div>
                    <div class="text-xs text-neutral-500">{{ item.desc }}</div>
                </a>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const bookmarkGroups = [
    {
        title: "Favorites",
        items: [
            { name: "Duolingo", url: "https://www.duolingo.com/", desc: "Language Learning" },
            { name: "Twitter", url: "https://twitter.com/", desc: "Social Platform" },
            { name: "YouTube", url: "https://youtube.com/", desc: "Video Platform" },
            { name: "Twitch", url: "https://twitch.tv/", desc: "Live Streaming" },
            { name: "V2EX", url: "https://www.v2ex.com/", desc: "Tech Community" },
            { name: "llc", url: "#", desc: "" },
        ],
    },
    {
        title: "Tools",
        items: [
            { name: "Editor | JSON Crack", url: "https://jsoncrack.com/", desc: "Online JSON Visualizer" },
            { name: "drawDB", url: "https://drawdb.com/", desc: "Database Design Tool" },
            { name: "Copyright", url: "#", desc: "" },
            { name: "Xuehang's Workbench", url: "#", desc: "" },
        ],
    },
    {
        title: "VPN",
        items: [
            { name: "V2free", url: "https://www.v2free.net/", desc: "Free V2ray/SS Nodes" },
            { name: "Shadowrocket", url: "https://shadowrocket.com/", desc: "iOS VPN" },
        ],
    },
    {
        title: "USDT",
        items: [
            { name: "Binance", url: "https://www.binance.com/", desc: "Crypto Exchange" },
            { name: "Depay", url: "https://depay.com/", desc: "Crypto MasterCard" },
        ],
    },
    {
        title: "Python",
        items: [
            { name: "Welcome to Python.org", url: "https://www.python.org/", desc: "Official Python" },
            { name: "mkdocs-material", url: "https://squidfunk.github.io/mkdocs-material/", desc: "Documentation Generator" },
        ],
    },
    {
        title: "Deep Learning",
        items: [
            { name: "GitHub Copilot", url: "https://github.com/features/copilot", desc: "AI Coding Assistant" },
            { name: "Hugging Face", url: "https://huggingface.co/", desc: "AI Community" },
        ],
    },
    // ...add more groups as needed
];
</script>

<style scoped>
/* 可根据需要补充自定义样式 */
</style>