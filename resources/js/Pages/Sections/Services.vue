<template>
    <div id="servicios" class="bg-white">
      <!-- Header -->
      <div class="relative bg-gray-800 pb-32">
        <div class="absolute inset-0">
          <img class="h-full w-full object-cover" src="/images/service-bg.jpg" alt="" />
          <div class="absolute inset-0 bg-yellow-800 mix-blend-multiply" aria-hidden="true" />
        </div>
        <div class="relative mx-auto max-w-7xl py-24 px-6 sm:py-32 lg:px-8">
          <h1 class="text-4xl font-bold tracking-tight text-white md:text-5xl lg:text-6xl">Servicios</h1>
          <p class="mt-6 max-w-3xl text-xl text-gray-300">Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames. Dui, amet, nec sit pulvinar.</p>
        </div>
      </div>

      <!-- Overlapping cards -->
      <section class="relative z-10 mx-auto -mt-32 max-w-7xl px-6 lg:px-8" aria-labelledby="contact-heading">
        <h2 class="sr-only" id="contact-heading">Contact us</h2>
        <div class="grid grid-cols-1 gap-y-20 lg:grid-cols-3 lg:gap-y-0 lg:gap-x-8">
          <div v-for="link in supportLinks" :key="link.name" class="flex flex-col rounded-2xl bg-white shadow-xl">
            <div class="relative flex-1 px-6 pt-16 pb-8 md:px-8">
              <div class="absolute top-0 inline-block -translate-y-1/2 transform rounded-xl bg-yellow-600 p-5 shadow-lg">
                <component :is="link.icon" class="h-6 w-6 text-white" aria-hidden="true" />
              </div>
              <h3 class="text-xl font-medium text-gray-900">{{ link.name }}</h3>
              <p class="mt-4 text-base text-gray-500">{{ link.description }}</p>
            </div>
            <div class="rounded-bl-2xl rounded-br-2xl bg-gray-50 p-6 md:px-8">
              <a :href="link.href" class="text-base font-medium text-yellow-700 hover:text-yellow-600">Hablemos<span aria-hidden="true"> &rarr;</span></a>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>

  <script setup>
  import { LifebuoyIcon, NewspaperIcon, PhoneIcon } from '@heroicons/vue/24/outline'

  const supportLinks = [
    {
      name: 'Sales',
      href: '#contacto',
      description:
        'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      icon: PhoneIcon,
    },
    {
      name: 'Technical Support',
      href: '#contacto',
      description:
        'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      icon: LifebuoyIcon,
    },
    {
      name: 'Media Inquiries',
      href: '#contacto',
      description:
        'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      icon: NewspaperIcon,
    },
  ]
  </script>
