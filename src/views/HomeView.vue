<script setup lang="ts">
</script>

<template>
    <!-- 内容容器已在 App.vue 提供，这里只保留页面内容结构 -->
    <!-- Hero -->
    <section class="py-16 sm:py-24">
        <div class="flex flex-col sm:flex-row items-center sm:items-start space-y-4 sm:space-y-0 sm:space-x-8">
            <div class="flex-1">
                <p class="text-base text-neutral-600">ᠠᠪᡴᠠ ᡨᠠᠴᡳᠮᠪᡳ ᡩᠣᠣᠮᠪᡳ</p>
                <h1 class="text-4xl sm:text-5xl font-semibold tracking-tight">Abka TacimbiDoombi</h1>
                <p class="text-xl text-neutral-700">Life is short, you need Python!</p>
                <div class="pt-2 flex flex-wrap gap-3">
                    <a href="mailto:TacimbiDoombi@outlook.com"
                        class="inline-flex items-center rounded-lg border border-neutral-300 px-4 py-2 text-sm font-medium hover:bg-neutral-50">Email</a>
                    <a href="https://github.com/TacimbiDoombi" target="_blank" rel="noopener"
                        class="inline-flex items-center rounded-lg px-4 py-2 text-sm font-medium text-neutral-700 hover:text-neutral-900">GitHub</a>
                    <a href="https://huggingface.co/TacimbiDoombi" target="_blank" rel="noopener"
                        class="inline-flex items-center rounded-lg px-4 py-2 text-sm font-medium text-neutral-700 hover:text-neutral-900">Hugging
                        Face</a>
                </div>
            </div>
            <div class="shrink-0 mt-6 sm:mt-0">
                <img src="/logo.png" alt="Cover" class="w-40 h-40 object-cover rounded-xl shadow" />
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="py-10">
        <div class="rounded-xl border border-neutral-200 bg-white p-6">
            <h2 class="text-xl font-medium">About Me</h2>
            <p class="mt-3 text-neutral-700">I love Python and open source, aiming for simplicity and reliability. I
                focus on building clean, maintainable frontends with Tailwind CSS.</p>
        </div>
    </section>

    <!-- Skills -->
    <section id="skills" class="py-10">
        <h2 class="text-xl font-medium">Skills</h2>
        <div class="mt-4 flex flex-wrap gap-3">
            <span
                class="inline-flex items-center rounded-full bg-neutral-100 px-3 py-1 text-sm text-neutral-700">Python</span>
            <span
                class="inline-flex items-center rounded-full bg-neutral-100 px-3 py-1 text-sm text-neutral-700">Tailwind
                CSS</span>
            <span class="inline-flex items-center rounded-full bg-neutral-100 px-3 py-1 text-sm text-neutral-700">GitHub
                Pages</span>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="py-10">
        <div class="rounded-xl border border-neutral-200 bg-white p-6">
            <h2 class="text-xl font-medium">Contact</h2>
            <p class="mt-3 text-neutral-700">Email:
                <a class="text-neutral-900 underline underline-offset-4 hover:no-underline"
                    href="mailto:TacimbiDoombi@outlook.com">TacimbiDoombi@outlook.com</a>
            </p>
            <p class="mt-2 text-neutral-700">Profiles:
                <a class="text-neutral-900 underline underline-offset-4 hover:no-underline"
                    href="https://github.com/TacimbiDoombi" target="_blank" rel="noopener">GitHub</a>
                ·
                <a class="text-neutral-900 underline underline-offset-4 hover:no-underline"
                    href="https://huggingface.co/TacimbiDoombi" target="_blank" rel="noopener">Hugging Face</a>
            </p>
        </div>
    </section>

</template>
