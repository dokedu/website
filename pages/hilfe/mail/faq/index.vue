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
            <h1>FAQ</h1>


            <div itemscope itemprop="mainEntity" itemtype="https://schema.org/Question">
                <h2 itemprop="name">Warum unterstützt Dokedu Mail kein POP3?</h2>
                <div itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer">
                    <div itemprop="text">
                        <p>
                            POP3 ist eine ältere Technologie, die verwendet wird, um E-Mails von einem Server
                            herunterzuladen. Bei
                            Dokedu Mail haben wir uns allerdings dafür entschieden, diese Technologie nicht zu unterstützen.
                        </p>

                        <p>
                            Einer der Hauptgründe dafür ist, dass POP3 in vielen Fällen nicht die beste Erfahrung für die
                            Benutzer
                            bietet. Mit POP3 werden E-Mails von unserem Server auf dein Gerät heruntergeladen und dann
                            normalerweise vom
                            Server gelöscht. Das bedeutet, dass, wenn du von einem anderen Gerät auf deine E-Mails zugreifen
                            möchtest,
                            diese möglicherweise nicht verfügbar sind. Diese Limitierung hat zur Entscheidung geführt, POP3
                            nicht zu
                            unterstützen.
                        </p>

                        <p>Stattdessen unterstützen wir IMAP. IMAP ist eine modernere Technologie, die es ermöglicht, dass
                            deine
                            E-Mails auf all deinen Geräten synchronisiert werden. Du kannst auf alle deine E-Mails
                            zugreifen, egal, ob
                            du dein Handy, deinen Computer oder eine Web-Oberfläche verwendest.
                        </p>
                    </div>
                </div>

            </div>

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