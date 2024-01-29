<template>
    <main class="prose-stone prose mx-auto max-w-3xl p-12">
        <section>
            <p>
                <small>
                    <nuxt-link href="/hilfe">Hilfe</nuxt-link>
                    <span class="mx-1">/</span>
                    <nuxt-link href="/hilfe/mail">Mail</nuxt-link>
                    <span class="mx-1">/</span>
                    <nuxt-link href="/hilfe/mail/setup">Hilfe</nuxt-link>
                </small>
            </p>
            <h1>iPhone</h1>

            <h2>Apple Mail</h2>

            <video controls class="max-h-[800px] mx-auto rounded-lg">
                <source src="/videos/hilfe/mail/ios.mp4" type="video/mp4">
            </video>
        </section>
    </main>
</template>

<script lang="ts" setup>

useSeoMeta({
    title: 'Dokedu - Die digitale Lösung für Ihren Schulalltag',
})

useHead({
    htmlAttrs: {
        lang: 'de'
    },
    link: [
        {
            rel: 'icon',
            type: 'image/png',
            href: '/favicon.ico'
        }
    ]
})
</script>