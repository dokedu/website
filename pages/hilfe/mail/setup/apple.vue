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
            <h1>Apple Mail</h1>

            <p>Bitte folgen Sie den unten aufgeführten Schritten, um ein IMAP-Konto in Apple Mail einzurichten:</p>

            <ol>
                <li>Öffnen Sie Apple Mail.</li>

                <li>Gehen Sie zu "Mail" in der oberen Menüleiste und wählen Sie "Accounts" aus.</li>

                <li>Ein neues Fenster mit der Überschrift "Internet Accounts" öffnet sich. Klicken Sie dort auf das "+"
                    Symbol
                    am unteren Rand.</li>

                <li>Sie sehen nun verschiedene Optionen für E-Mail-Anbieter. Wenn Ihr Anbieter aufgeführt ist, wählen Sie
                    ihn
                    aus. Falls nicht, wählen Sie "Anderer Mail-Account...".</li>

                <li>Geben Sie Ihren Namen, Ihre E-Mail-Adresse und Ihr Passwort ein und klicken Sie auf "Anmelden".</li>

                <li>Apple Mail versucht nun, die Einstellungen automatisch zu finden. Falls dies nicht gelingt, müssten Sie
                    die
                    folgenden Einstellungen manuell eingeben:

                    <ul>
                        <li>Kontotyp: Wählen Sie "IMAP".</li>
                        <li>Posteingangsserver: Hier geben Sie den Namen Ihres IMAP-Servers ein (mail.dokedu.org).</li>
                        <li>Postausgangsserver: Hier geben Sie den Namen Ihres SMTP-Servers ein (mail.dokedu.org).</li>
                    </ul>
                </li>

                <li>Klicken Sie auf "Anmelden". Ihr IMAP-Konto sollte nun in Apple Mail eingerichtet sein.</li>
            </ol>

            <p>Bei weiteren Fragen oder Unklarheiten stehen wir Ihnen gerne zur Verfügung.</p>

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