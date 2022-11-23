<template>
   <section class="bg-blue" id="about-cta">
      <div class="gap-16 items-center py-8 px-4 mx-auto max-w-screen-xl lg:grid lg:grid-cols-2 lg:py-16 lg:px-6" v-for="item in items" :key="item.title">
        <div class="font-light sm:text-lg">
          <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-white">{{item.title}}</h2>
          <p class="mb-4 text-white">
            {{item.paragraphOne}}
          </p>
          <p class="text-white">
            {{item.paragraphTwo}}
          </p>
          <a
            :href="item.buttonLink" 
            class="
              inline-flex
              items-center
              justify-center
              px-5
              py-3
              mr-3
              mt-3
              text-blue
              font-medium
              text-center
              rounded-lg
              bg-white
              hover:ring-4
              focus:ring-4 focus:ring-primary-300
              dark:focus:ring-primary-900
            "
          >
            {{item.buttonText}}
            <svg class="w-5 h-5 ml-2 -mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                fill-rule="evenodd"
                d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </a>
        </div>
        <div class="grid grid-cols-2 gap-4 mt-8">
          <img
            class="w-full rounded-lg"
            :src="require(`~/assets/images/${item.photoOne}`)" 
            alt=""
          />
          <img
            class="mt-4 w-full lg:mt-10 rounded-lg"
            :src="require(`~/assets/images/${item.photoTwo}`)" 
            alt=""
          />
        </div>
      </div>
    </section>
</template>



<script>
    export default {
      name: 'TextWithImage',
  
      props: {
        title: {
          type: String
        },
        paragraphOne: {
          type: String
        },
        paragraphTwo: {
          type: String
        },
        buttonLink: {
          type: String
        },
  
        buttonText: {
          type: String
        },
        photoOne: {
          type: String
        },
        photoTwo: {
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
    