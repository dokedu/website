<template>
    <main class="prose-stone prose mx-auto max-w-3xl p-12">
        <section>
            <p>
                <small>
                    <nuxt-link href="/hilfe">Hilfe</nuxt-link>
                    <span class="mx-1">/</span>
                    <nuxt-link href="/hilfe/mail">Mail</nuxt-link>
                </small>
            </p>
            <h1>Setup</h1>

            <ul>
                <li><nuxt-link to="/hilfe/mail/setup/outlook">Outlook</nuxt-link></li>
                <li><nuxt-link to="/hilfe/mail/setup/windows">Windows Mail</nuxt-link></li>
                <li><nuxt-link to="/hilfe/mail/setup/iphone">iPhone</nuxt-link></li>
                <li><nuxt-link to="/hilfe/mail/setup/apple">Apple Mail</nuxt-link></li>
                <li><nuxt-link to="/hilfe/mail/setup/thunderbird">Thunderbird</nuxt-link></li>
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