<!--
  This example requires some changes to your config:

  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/aspect-ratio'),
    ],
  }
  ```
-->
<template>
    <div id="proyectos" class="bg-white">
      <div class="mx-auto max-w-7xl py-12 px-6 lg:px-8 lg:py-24">
        <div class="space-y-12">
          <div class="space-y-5 sm:space-y-4 md:max-w-xl lg:max-w-3xl xl:max-w-none">
            <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Proyectos</h2>
            <p class="text-xl text-gray-500">Odio nisi, lectus dis nulla. Ultrices maecenas vitae rutrum dolor ultricies donec risus sodales. Tempus quis et.</p>
          </div>
          <ul role="list" class="space-y-12 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-12 sm:space-y-0 lg:grid-cols-3 lg:gap-x-8">
            <li v-for="person in people" :key="person.name">
              <div class="space-y-4">
                <div class="aspect-w-3 aspect-h-2">
                  <img class="rounded-lg object-cover shadow-lg" :src="person.imageUrl" alt="" />
                </div>

                <div class="space-y-2">
                  <div class="space-y-1 text-lg font-medium leading-6">
                    <h3>{{ person.name }}</h3>
                    <p class="text-yellow-600">{{ person.company }}</p>
                    <p class="mt-4 pt-4 text-base text-gray-500">{{ person.description }}</p>
                  </div>
                  <ul role="list" class="flex space-x-5">
                    <li>
                      <a :href="person.url" class="text-gray-400 hover:text-gray-500">
                        <span class="sr-only">Twitter</span>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M13.19 8.688a4.5 4.5 0 011.242 7.244l-4.5 4.5a4.5 4.5 0 01-6.364-6.364l1.757-1.757m13.35-.622l1.757-1.757a4.5 4.5 0 00-6.364-6.364l-4.5 4.5a4.5 4.5 0 001.242 7.244" />
                            </svg>
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </template>

  <script setup>
  const people = [
    {
      name: 'Odio nisi, lectus dis nulla',
      company: 'Carozzi',
      description: 'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      imageUrl:
        '/images/proyectos/07_img.jpg',
      url: '#',
    },
    {
      name: 'Odio nisi, lectus dis nulla',
      company: 'Carozzi',
      description: 'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      imageUrl:
        '/images/proyectos/08_img.jpg',
      url: '#',
    },
    {
      name: 'Odio nisi, lectus dis nulla',
      company: 'Carozzi',
      description: 'Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.',
      imageUrl:
        '/images/proyectos/10_img.jpg',
      url: '#',
    },
    // More people...
  ]
  </script>
