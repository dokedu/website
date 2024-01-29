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
            <h1>Thunderbird</h1>

            <ol>
                <li>
                    <p><strong>Thunderbird öffnen</strong></p>
                    <ul>
                        <li>Öffnen Sie zunächst Ihr Thunderbird-Mail-Programm. </li>
                    </ul>
                </li>
                <li>
                    <p><strong>Konto-Einstellungen</strong></p>
                    <ul>
                        <li>Navigieren Sie zu den <code>Kontoeinstellungen</code> durch Klick auf <code>Extras</code> in der
                            Menüleiste. Falls Sie die Menüleiste nicht sehen, drücken Sie die <code>Alt</code> Taste auf
                            Ihrer Tastatur.</li>
                    </ul>
                </li>
                <li>
                    <p><strong>Neues Konto hinzufügen</strong></p>
                    <ul>
                        <li>Klicken Sie auf <code>Kontoeinstellungen</code> und dann auf <code>Konto-Aktionen</code> unten
                            links im Fenster.</li>
                        <li>Wählen Sie <code>Mail-Konto hinzufügen</code>.</li>
                    </ul>
                </li>
                <li>
                    <p><strong>Benutzerinformationen</strong></p>
                    <ul>
                        <li>Geben Sie Ihren Namen, Ihre E-Mail-Adresse und Ihr Passwort ein und klicken Sie auf
                            <code>Weiter</code>.
                        </li>
                    </ul>
                </li>
                <li>
                    <p><strong>Server-Einstellungen</strong></p>
                    <ul>
                        <li>Thunderbird wird versuchen, die Kontoeinstellungen automatisch zu finden. Falls das nicht
                            möglich ist, geben Sie bitte folgende Informationen ein:<ul>
                                <li>IMAP-Server: mail.dokedu.org</li>
                                <li>Port: 993 (Standard für IMAP)</li>
                                <li>Sicherheit: SSL/TLS</li>
                                <li>Authentifizierung: Passwort, normal</li>
                            </ul>
                        </li>
                    </ul>
                </li>
                <li>
                    <p><strong>Kontoeinrichtung abschließen</strong></p>
                    <ul>
                        <li>Klicken Sie auf <code>Fertig</code> um die Einrichtung abzuschließen. Thunderbird wird nun Ihre
                            E-Mails vom Server abrufen.</li>
                    </ul>
                </li>
            </ol>

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