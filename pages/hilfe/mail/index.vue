<template>
    <main class="prose-stone prose mx-auto max-w-3xl p-12">
        <section>
            <p>
                <small>
                    <nuxt-link href="/hilfe">Hilfe</nuxt-link>
                </small>
            </p>
            <h1>Mail</h1>

            <ul>
                <li>
                    <nuxt-link to="/hilfe/mail/setup">Setup</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/hilfe/mail/faq">FAQ</nuxt-link>
                </li>
            </ul>
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