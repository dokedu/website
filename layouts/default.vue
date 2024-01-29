<template>
    <PageHeader />
    <slot />

    <footer class="prose mx-auto max-w-3xl p-12 text-sm prose-stone">
        <p class="flex gap-3 flex-wrap">
            <nuxt-link to="/">Start</nuxt-link>
            <nuxt-link to="/impressum">Impressum</nuxt-link>
            <nuxt-link to="/datenschutz">Datenschutz</nuxt-link>
            <nuxt-link to="/agb">AGB</nuxt-link>
            <nuxt-link to="/hilfe">Hilfe</nuxt-link>
            <a href="https://status.dokedu.org" target="_blank">Status</a>
            <a href="mailto:support@dokedu.org">Support</a>
        </p>
        <p>© 2024 Dokedu UG (haftungsbeschränkt). Alle Rechte vorbehalten.</p>
    </footer>
</template>
