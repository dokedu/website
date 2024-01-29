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
            <h1>Outlook</h1>


            <video controls class="rounded-md">
                <source src="/videos/hilfe/mail/outlook.mp4" type="video/mp4">
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