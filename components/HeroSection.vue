<template>
    <section class="" id="home-hero">
      <div class="grid max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12" v-for="item in items" :key="item.title">
        <div class="mr-auto place-self-center lg:col-span-6">
          <h1 class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl">
            {{item.title}}
          </h1>

          <h2 class="subtitle max-w-2xl mb-4 text-4xl font-bold tracking-tight leading-none md:text-2xl xl:text-2xl">
            {{item.subhead}}
          </h2>
          <p class="max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400">
            {{item.text}}
          </p>
          <a
            href="tel:440-285-4357"
            class="
              inline-flex
              items-center
              justify-center
              px-5
              py-3
              mr-3
              text-base
              font-medium
              text-center text-white
              rounded-lg
              bg-primary-700
              hover:bg-primary-800
              focus:ring-4 focus:ring-primary-300
              dark:focus:ring-primary-900
            "
          >
            Call us now
            <svg class="w-5 h-5 ml-2 -mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                fill-rule="evenodd"
                d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </a>
          <a
            :href="item.buttonLink" 
            class="
              inline-flex
              items-center
              justify-center
              px-5
              py-3
              text-base
              font-medium
              text-center text-gray-900
              border border-gray-300
              rounded-lg
              hover:bg-gray-100
              focus:ring-4 focus:ring-gray-100
              dark:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:focus:ring-gray-800
            "
          >
            {{item.buttonText}}
          </a>
        </div>
        <div class="mt-8 lg:mt-0 lg:col-span-6 lg:flex">
          <img :src="require(`~/assets/images/${item.photo}`)"  class="intro-img" alt="" loading="lazy" />
        </div>
      </div>
    </section>
 </template>
 
 
 
 <script>
     export default {
       name: 'HeroSection',
   
       props: {
         title: {
           type: String
         },
         subhead: {
           type: String
         },
         text: {
           type: String
         },
         buttonLink: {
           type: String
         },
   
         buttonText: {
           type: String
         },
         photo: {
           type: String
         },
         
         items: {
           type: Array
         }
       }
     }
 </script>
     
 
 <style lang="postcss" scoped>
 
 
 </style>
     