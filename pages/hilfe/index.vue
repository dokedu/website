<template>
    <main class="prose-stone prose mx-auto max-w-3xl p-12">
        <section>
            <h1>Hilfe</h1>

            <p>Bitte wählen Sie eine Anwendung, bei der Sie Hilfe benötigen:</p>

            <ul>
                <li>
                    <nuxt-link to="/hilfe/mail">Mail</nuxt-link>
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