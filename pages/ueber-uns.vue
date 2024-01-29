<template>
    <div class="bg-white py-24 sm:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl sm:text-center">
                <h2 class="text-3xl font-bold tracking-tight text-stone-900 sm:text-4xl">Über uns</h2>
                <p class="mt-6 text-lg leading-8 text-stone-600">Unser Ziel ist es, eine effiziente Verwaltung von
                    Lernfortschritten zu ermöglichen und die Bewertung von
                    Schülerleistungen zu digitalisieren. Wir wollen Pädagogen dabei unterstützen, Lernbeobachtungen zu
                    erfassen und
                    sie digital mit den offiziellen Kompetenzen des jeweiligen Bundeslandes zu verknüpfen.</p>
            </div>
            <ul role="list"
                class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-6 gap-y-20 sm:grid-cols-2 lg:max-w-4xl lg:gap-x-8 xl:max-w-none">
                <li v-for="person in people" :key="person.name" class="flex flex-col gap-6 xl:flex-row">
                    <img class="aspect-[4/5] w-52 flex-none rounded-2xl object-cover" :src="person.imageUrl" alt="" />
                    <div class="flex-auto">
                        <h3 class="text-lg font-semibold leading-8 tracking-tight text-stone-900">{{ person.name }}</h3>
                        <p class="text-base leading-7 text-stone-600">{{ person.role }}</p>
                        <p class="mt-6 text-base leading-7 text-stone-600">{{ person.bio }}</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>



<script setup>
const people = [
    {
        name: 'Tom Härter',
        role: 'Gründer',
        imageUrl: '/img/team/tom.jpeg',
        bio: 'Tom Härter, der Gründer von Dokedu, verbindet sein Software-Fachwissen mit seiner Leidenschaft für modernste Bildungstechnologie. Da er selbst eine alternative Schule besucht hat, hat seine innovative Führung Dokedu in eine zuverlässige Plattform verwandelt, die die Bildung für viele verbessert.',
    },
    {
        name: 'Leonhard Kobbe',
        role: 'Verkauf & Marketing',
        imageUrl: '/img/team/leonhard.jpg',
        bio: 'Leonhard Kobbe, steht mit seinem reichen Erfahrungsschatz im Verkauf & Marketing und dem tiefen Verständnis für die Bedürfnisse unserer Kunden an vorderster Front, um die Lösungen von Dokedu zielorientiert zu vermarkten.',
    },
    {
        name: 'Aaron Mahlke',
        role: 'Designer',
        imageUrl: '/img/team/aaron.jpeg',
        bio: 'Aaron Mahlke, unser Designer, ist verantwortlich für die visuelle Darstellung unseres Produkts. Er stellt sicher, dass Dokedu nicht nur funktional, sondern auch ästhetisch ansprechend und benutzerfreundlich ist.',
    },
    {
        name: 'Šimon Benčík',
        role: 'Junior Full-Stack-Ingenieur',
        imageUrl: '/img/team/simon.jpeg',
        bio: 'Šimon Benčík ist ein Junior Full-Stack-Ingenieur in unserem Team. Seine Rolle als Entwickler ist entscheidend für unsere Produktentwicklung. Er arbeitet unermüdlich daran, die Funktionalität und Leistung unserer digitalen Plattform ständig zu verbessern, um den Bedürfnissen unserer Benutzer gerecht zu werden.',
    },
    {
        name: 'Adrian Jakob',
        role: 'Full-Stack-Ingenieur',
        imageUrl: '/img/team/adrian.jpeg',
        bio: 'Adrian Jakob, ein Full-Stack-Ingenieur in unserem Team, ist ebenfalls ein wichtiger Bestandteil unserer Produktentwicklung. Als erfahrener Entwickler setzt er sich ständig dafür ein, die Qualität unserer digitalen Plattform zu optimieren und die Erwartungen unserer Benutzer zu erfüllen.',
    },
    {
        name: 'Lars Graf',
        role: 'Berater',
        imageUrl: '/img/team/lars.jpg',
        bio: 'Last but not least ist Lars Graf, unser Berater, der seine wertvolle Erfahrung und sein Fachwissen einbringt, um die strategische Ausrichtung von Dokedu weiterzuentwickeln. Mit einer Waldorf-Ausbildung und jahrelanger Erfahrung im Silicon Valley bringt er ein breites Spektrum an Wissen und innovativen Ansätzen mit, um sicherzustellen, dass Dokedu einen Mehrwert für unsere Nutzer schafft.',
    },
]
</script>