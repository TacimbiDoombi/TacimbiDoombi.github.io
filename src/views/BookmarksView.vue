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
            { name: "Google Translate", url: "https://translate.google.com/", desc: "Online Translation" },
            { name: "Twitter", url: "https://twitter.com/", desc: "Social Platform" },
            { name: "哔哩哔哩", url: "https://www.bilibili.com/", desc: "Video Platform" },
            { name: "YouTube", url: "https://youtube.com/", desc: "Video Platform" },
            { name: "Twitch", url: "https://twitch.tv/", desc: "Live Streaming Platform" },
            { name: "V2EX", url: "https://www.v2ex.com/", desc: "Tech Community Forum" },
            { name: "Duolingo", url: "https://www.duolingo.com/", desc: "Language Learning" },
            { name: "TLD-List", url: "https://tld-list.com/", desc: "Domain Extension Directory" },
            { name: "Zero To Mastery", url: "https://zerotomastery.io/", desc: "Online Learning Platform" },
            { name: "drawDB.app", url: "https://www.drawdb.app", desc: "Database Design Tool" },
            { name: "Creative Commons", url: "https://creativecommons.org", desc: "版权协议" },
            { name: "Chalk.ist", url: "https://chalk.ist", desc: "在线白板" },
            { name: "Linux.do", url: "https://linux.do/", desc: "Linux Community Forum" },
            { name: "Product Hunt", url: "https://www.producthunt.com", desc: "Discover New Products" },
            { name: "MongoDB 官方文档（安装）", url: "https://www.mongodb.com/zh-cn/docs/manual/administration/install-community/?linux-distribution=ubuntu&linux-package=default&operating-system=linux&search-linux=with-search-linux#std-label-install-mdb-community-ubuntu", desc: "MongoDB 安装文档" },
            { name: "Ubuntu root login", url: "https://cloud.tencent.com/document/product/1207/44569#ubuntu-.E7.B3.BB.E7.BB.9F.E5.A6.82.E4.BD.BF.E7.94.A8-root-.E7.94.A8.E6.88.B7.E7.99.BB.E5.BD.95.E5.AE.9E.E4.BE.8B.EF.BC.9F", desc: "腾讯云 Ubuntu root 登录说明" },
            { name: "Google Stitch", url: "https://stitch.withgoogle.com/", desc: "Google Stitch 服务" },
            { name: "Linktree", url: "https://linktr.ee", desc: "Social Links Aggregator" },
        ],
    },
    {
        title: "Tools",
        items: [
            { name: "Editor | JSON Crack", url: "https://jsoncrack.com/", desc: "Online JSON Visualizer" },
            { name: "drawDB", url: "https://drawdb.com/", desc: "Database Design Tool" },
            { name: "Favicon.io", url: "https://favicon.io", desc: "Favicon Generator" },
            { name: "ItangTalk", url: "https://itangtalk.com", desc: "Online Community" },
            { name: "Copyright", url: "#", desc: "" },
            { name: "Xuehang's Workbench", url: "#", desc: "" },
            { name: "LatexLive", url: "https://www.latexlive.com", desc: "Online LaTeX Editor" },
            { name: "Automate PyPI Releases with GitHub Actions", url: "https://medium.com/@VersuS_/automate-pypi-releases-with-github-actions-4c5a9cfe947d", desc: "PyPI Release Automation Guide" },
        ],
    },
    {
        title: "Finance",
        items: [
            { name: "Stripe", url: "https://stripe.com", desc: "Online Payments" },
            { name: "Mercury", url: "https://mercury.com", desc: "Business Banking" },
            { name: "Capital One", url: "https://www.capitalone.com", desc: "Banking & Credit Cards" },
            { name: "FasterPay", url: "https://fasterpay.com", desc: "Global Payments" },
            { name: "iFastGB", url: "https://www.ifastgb.com/zh/home", desc: "Financial Services" },
            { name: "Fiverr", url: "https://www.fiverr.com", desc: "Freelance Marketplace" },
            { name: "Stable", url: "https://usestable.com", desc: "Business Banking" },
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
            { name: "Python Community Forum", url: "https://discuss.python.org", desc: "Python Discussions" },
            { name: "mkdocs-material", url: "https://squidfunk.github.io/mkdocs-material/", desc: "Documentation Generator" },
            { name: "PyTorch", url: "https://pytorch.org", desc: "Deep Learning Framework" },
            { name: "Colab", url: "https://colab.research.google.com", desc: "Google Colab Notebook" },
            { name: "Kaggle", url: "https://www.kaggle.com", desc: "Data Science Community" },
            { name: "D2L (动手学深度学习)", url: "https://zh-v2.d2l.ai", desc: "Deep Learning Book" },
        ],
    },
    {
        title: "Deep Learning",
        items: [
            { name: "GitHub Copilot", url: "https://github.com/features/copilot", desc: "AI Coding Assistant" },
            { name: "Hugging Face", url: "https://huggingface.co/", desc: "AI Community" },
            { name: "OpenRouter", url: "https://openrouter.ai/models", desc: "AI Model Hub" },
            { name: "Fal.ai", url: "https://fal.ai", desc: "AI Platform" },
            { name: "Unsloth", url: "https://docs.unsloth.ai", desc: "Efficient LLM Training" },
            { name: "ModelScope", url: "https://modelscope.cn/home", desc: "AI Model Hub" },
            { name: "Heywhale", url: "https://www.heywhale.com/home", desc: "AI Data Platform" },
            { name: "JarvisLabs", url: "https://jarvislabs.ai", desc: "AI Compute Platform" },
            { name: "ArtificialAnalysis", url: "https://artificialanalysis.ai", desc: "AI Analysis Platform" },
            { name: "RunPod", url: "https://console.runpod.io", desc: "AI Compute Platform" },
        ],
    },
    {
        title: "Research & Papers",
        items: [
            { name: "arXiv", url: "https://arxiv.org", desc: "Preprint Papers" },
            { name: "ORCID", url: "https://orcid.org", desc: "Researcher ID" },
        ],
    },
    {
        title: "APIs & Platforms",
        items: [
            { name: "OpenAI Platform", url: "https://platform.openai.com/chat/edit", desc: "OpenAI API Playground" },
            { name: "OpenAI Cookbook", url: "https://cookbook.openai.com", desc: "OpenAI API Cookbook" },
        ],
    },
    {
        title: "GitHub",
        items: [
            { name: "GitHub Copilot", url: "https://github.com/copilot", desc: "Copilot Product Page" },
        ],
    },
    {
        title: "Logistics",
        items: [
            { name: "USPS", url: "https://zh.usps.com", desc: "US Postal Service (Chinese)" },
        ],
    },
    {
        title: "Learning",
        items: [
            { name: "Microsoft AI Agents for Beginners", url: "https://microsoft.github.io/ai-agents-for-beginners/translations/zh/", desc: "AI Agents Learning Resource" },
        ],
    },
    // ...add more groups as needed
];
</script>

<style scoped>
/* 可根据需要补充自定义样式 */
</style>