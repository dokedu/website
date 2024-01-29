<template>
    <header class="bg-white">
        <nav class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8" aria-label="Global">

            <div class="flex gap-12 items-center">
                <div class="flex lg:flex-1">
                    <nuxt-link href="/" class="-m-1.5 p-1.5">
                        <span class="sr-only">Dokedu</span>
                        <img class="h-8 w-auto" src="/img/logo.svg" alt="" />
                    </nuxt-link>
                </div>
                <PopoverGroup class="hidden lg:flex lg:gap-x-12">
                    <Popover class="relative">
                        <PopoverButton class="flex items-center gap-x-1 text-base font-semibold leading-6 text-stone-900">
                            Produkte
                            <ChevronDownIcon class="h-5 w-5 flex-none text-stone-400" aria-hidden="true" />
                        </PopoverButton>

                        <transition enter-active-class="transition ease-out duration-200"
                            enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0"
                            leave-active-class="transition ease-in duration-150"
                            leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
                            <PopoverPanel
                                class="absolute -left-8 top-full z-10 mt-3 w-screen max-w-md overflow-hidden rounded-3xl bg-white shadow-lg ring-1 ring-stone-900/5">
                                <div class="p-4">
                                    <div v-for="item in products" :key="item.name"
                                        class="group relative flex items-center gap-x-6 rounded-lg p-4 text-base leading-6 hover:bg-stone-50">
                                        <div
                                            class="flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-stone-50 group-hover:bg-white">
                                            <component :is="item.icon"
                                                class="h-6 w-6 text-stone-600 group-hover:text-blue-600"
                                                aria-hidden="true" />
                                        </div>
                                        <div class="flex-auto">
                                            <a :href="item.href" class="block font-semibold text-stone-900">
                                                {{ item.name }}
                                                <span class="absolute inset-0" />
                                            </a>
                                            <p class="mt-1 text-stone-600">{{ item.description }}</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="grid grid-cols-2 divide-x divide-stone-900/5 bg-stone-50">
                                    <a v-for="item in callsToAction" :key="item.name" :href="item.href"
                                        class="flex items-center justify-center gap-x-2.5 p-3 text-base font-semibold leading-6 text-stone-900 hover:bg-stone-100">
                                        <component :is="item.icon" class="h-5 w-5 flex-none text-stone-400"
                                            aria-hidden="true" />
                                        {{ item.name }}
                                    </a>
                                </div>
                            </PopoverPanel>
                        </transition>
                    </Popover>

                    <nuxt-link to="/ueber-uns" class="text-base font-semibold leading-6 text-stone-900">Über uns</nuxt-link>

                    <nuxt-link to="/blog" class="text-base font-semibold leading-6 text-stone-900">
                        Blog
                    </nuxt-link>
                </PopoverGroup>
            </div>

            <div class="flex lg:hidden">

            </div>
            <div class="flex lg:hidden">
                <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-stone-700"
                    @click="mobileMenuOpen = true">
                    <span class="sr-only">Open main menu</span>
                    <Bars3Icon class="h-6 w-6" aria-hidden="true" />
                </button>
            </div>
            <div class="hidden lg:flex lg:flex-1 lg:justify-end">
                <a href="https://app.dokedu.org/login"
                    class="focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-neutral-950 transition-color group relative inline-flex h-fit select-none items-center justify-center gap-2 overflow-hidden rounded-lg border shadow-sm border-transparent bg-neutral-950 text-white hover:bg-neutral-700 px-4 py-2 text-sm">Anmelden
                    <span aria-hidden="true">&rarr;</span></a>
            </div>
        </nav>
        <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
            <div class="fixed inset-0 z-10" />
            <DialogPanel
                class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-stone-900/10">
                <div class="flex items-center justify-between">
                    <nuxt-link href="/" class="-m-1.5 p-1.5">
                        <span class="sr-only">Dokedu</span>
                        <img class="h-8 w-auto" src="/img/logo.svg" alt="" />
                    </nuxt-link>
                    <button type="button" class="-m-2.5 rounded-md p-2.5 text-stone-700" @click="mobileMenuOpen = false">
                        <span class="sr-only">Close menu</span>
                        <XMarkIcon class="h-6 w-6" aria-hidden="true" />
                    </button>
                </div>
                <div class="mt-6 flow-root">
                    <div class="-my-6 divide-y divide-stone-500/10">
                        <div class="space-y-2 py-6">
                            <Disclosure as="div" class="-mx-3" v-slot="{ open }">
                                <DisclosureButton
                                    class="flex w-full items-center justify-between rounded-lg py-2 pl-3 pr-3.5 text-base font-semibold leading-7 text-stone-900 hover:bg-stone-50">
                                    Produkt
                                    <ChevronDownIcon :class="[open ? 'rotate-180' : '', 'h-5 w-5 flex-none']"
                                        aria-hidden="true" />
                                </DisclosureButton>
                                <DisclosurePanel class="mt-2 space-y-2">
                                    <DisclosureButton v-for="item in [...products, ...callsToAction]" :key="item.name"
                                        as="a" :href="item.href"
                                        class="block rounded-lg py-2 pl-6 pr-3 text-base font-semibold leading-7 text-stone-900 hover:bg-stone-50">
                                        {{ item.name }}</DisclosureButton>
                                </DisclosurePanel>
                            </Disclosure>

                            <nuxt-link to="/ueber-uns"
                                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-stone-900 hover:bg-stone-50">
                                Über uns
                            </nuxt-link>

                            <nuxt-link to="/blog"
                                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-stone-900 hover:bg-stone-50">
                                Blog
                            </nuxt-link>
                        </div>
                        <div class="py-6">
                            <a href="https://app.dokedu.org/login" data-umami-event="login"
                                class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-stone-900 hover:bg-stone-50">
                                Anmelden
                            </a>
                        </div>
                    </div>
                </div>
            </DialogPanel>
        </Dialog>
    </header>
</template>

<script setup>
import { ref } from 'vue'
import {
    Dialog,
    DialogPanel,
    Disclosure,
    DisclosureButton,
    DisclosurePanel,
    Popover,
    PopoverButton,
    PopoverGroup,
    PopoverPanel,
} from '@headlessui/vue'
import {
    Bars3Icon,
    ArchiveBoxIcon,
    MicrophoneIcon,
    FingerPrintIcon,
    XMarkIcon,
    EnvelopeIcon,
} from '@heroicons/vue/24/outline'
import { ChevronDownIcon, PhoneIcon, PlayCircleIcon } from '@heroicons/vue/20/solid'

const products = [
    { name: 'Übersicht', description: 'Alle Produkte im Überblick', href: '/produkte', icon: Bars3Icon },
    { name: 'Mail', description: 'Mit Menschen verbinden', href: '/produkte/mail', icon: EnvelopeIcon },
    { name: 'Drive', description: 'Dateien sicher aufbewahren', href: '/produkte/drive', icon: ArchiveBoxIcon },
    { name: 'Dokumentation', description: 'Den Fortschritt im Auge behalten', href: '/produkte/record', icon: MicrophoneIcon },
]
const callsToAction = [
    { name: 'Demo ansehen', href: 'https://tally.so/r/wME2lg', icon: PlayCircleIcon },
    { name: 'Support kontaktieren', href: 'mailto:support@dokedu.org', icon: EnvelopeIcon },
]

const mobileMenuOpen = ref(false)
</script>