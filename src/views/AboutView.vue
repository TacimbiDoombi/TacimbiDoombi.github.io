<script setup lang="ts">
// English-only edition curated with the author's Manchu name.
const manchuName = 'ᠠᠪᡴᠠ ᡨᠠᠴᡳᠮᠪᡳ ᡩᠣᠣᠮᠪᡳ · Abka TacimbiDoombi'
const zen: string[] = [
    'Beautiful is better than ugly.',
    'Explicit is better than implicit.',
    'Simple is better than complex.',
    'Complex is better than complicated.',
    'Flat is better than nested.',
    'Sparse is better than dense.',
    'Readability counts.',
    "Special cases aren't special enough to break the rules.",
    'Although practicality beats purity.',
    'Errors should never pass silently.',
    'Unless explicitly silenced.',
    'In the face of ambiguity, refuse the temptation to guess.',
    'There should be one-- and preferably only one --obvious way to do it.',
    "Although that way may not be obvious at first unless you're Dutch.",
    'Now is better than never.',
    'Although never is often better than right now.',
    "If the implementation is hard to explain, it's a bad idea.",
    'If the implementation is easy to explain, it may be a good idea.',
    "Namespaces are one honking great idea -- let's do more of those!",
]
</script>

<template>
    <!-- 复用 App.vue 提供的主容器，只添加垂直留白 -->
    <div class="py-16">
        <!-- Header -->
        <section class="mb-12 space-y-3">
            <p class="text-base text-neutral-600">{{ manchuName }}</p>
            <h1 class="text-4xl sm:text-5xl font-semibold tracking-tight">The Zen of Python</h1>
            <p class="text-neutral-700 text-lg">From <span class="font-mono">import this</span> by Tim Peters — guiding
                principles that shape Python.</p>
            <p class="text-neutral-600 text-sm">Use these aphorisms in code reviews, design decisions, and daily
                practice.</p>
        </section>

        <!-- Aphorisms list -->
        <section class="space-y-6" aria-labelledby="zen-heading">
            <h2 id="zen-heading" class="sr-only">Zen Aphorisms</h2>
            <ol class="list-decimal pl-6 space-y-4">
                <li v-for="line in zen" :key="line" class="group">
                    <p class="font-medium text-neutral-900">{{ line }}</p>
                </li>
            </ol>
        </section>

        <!-- Footer note -->
        <section class="mt-12 rounded-xl border border-neutral-200 bg-white p-6">
            <h2 class="text-xl font-medium mb-3">Practice it</h2>
            <ul class="list-disc pl-5 space-y-2 text-neutral-700 text-sm">
                <li>In reviews, ask: can it be simpler and more readable?</li>
                <li>Avoid over-engineering: satisfy needs first, abstract later.</li>
                <li>When requirements are vague, clarify first—don’t guess.</li>
                <li>Surface errors with actionable logs/exceptions instead of swallowing them.</li>
                <li>Use namespaces (modules, packages, folders) to separate domains.</li>
            </ul>
            <p class="mt-4 text-neutral-500 text-xs">Aphorisms by Tim Peters (from "import this"). English-only edition
                curated by {{ manchuName }}.</p>
        </section>
    </div>
</template>

<style scoped>
/* 轻微的进入动画提升可读体验 */
ol>li {
    opacity: 0;
    transform: translateY(4px);
    animation: fadeIn 0.3s ease-out forwards;
}

@keyframes fadeIn {
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
</style>
