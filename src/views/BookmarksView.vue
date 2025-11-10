<template>
    <div class="min-h-screen text-gray-900 font-sans">
        <div class="mx-auto max-w-5xl px-4 py-8">
            <h1 class="text-3xl font-bold mb-6 text-center">Bookmark Navigation</h1>
            <div v-for="group in bookmarkGroups" :key="group.title" class="mb-10">
                <h2 class="text-xl font-semibold mb-4 text-gray-800">{{ group.title }}</h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
                    <a v-for="item in group.items" :key="item.name" :href="item.url" target="_blank" rel="noopener"
                        class="block bg-white rounded-xl shadow hover:shadow-lg transition p-4 border border-gray-100 hover:border-blue-400">
                        <div class="font-medium text-base mb-1">{{ item.name }}</div>
                        <div class="text-xs text-gray-500">{{ item.desc }}</div>
                    </a>
                </div>
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