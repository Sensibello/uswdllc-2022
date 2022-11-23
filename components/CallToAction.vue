<template>
  <section class="w-full mx-auto call-to-action cta">
        <div class="py-8 px-4 mx-auto max-w-screen-xl sm:py-16 lg:px-6" v-for="item in items" :key="item.title">
            <div class="mx-auto max-w-screen-sm text-center">
                <h2 class="mb-4 text-4xl font-extrabold tracking-tight text-white">{{ item.title }}</h2>
                <p class="mb-6 font-light text-white"> {{ item.subtitle }}</p>
                <a :href="item.buttonLink" class="hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm cta-btn">{{ item.buttonText }}</a>
            </div>
        </div>
    </section>
</template>
  
  <script>
  export default {
    name: 'CallToAction',

    props: {
      title: {
        type: String
      },
      subtitle: {
        type: String
      },
      buttonText: {
        type: String
      },
      buttonLink: {
        type: String
      },

      items: {
        type: Array
      }
    }
  }
  </script>
  

  <style lang="postcss" scoped>
.cta {
  position: relative;
  background-color: #1C263B;
    &:before {    
      content: "";
      background-image: url("~/assets/images/american-flag.png");
      background-size: contain;
      background-repeat: no-repeat;
      position: absolute;
      top: 0px;
      right: 0px;
      bottom: 0px;
      left: 0px;
      opacity: 0.3;
  }
}

/* .cta:before {    
    content: "";
    background-image: url("~/assets/images/american-flag.png");
    background-size: contain;
    position: absolute;
    top: 0px;
    right: 0px;
    bottom: 0px;
    left: 0px;
    opacity: 0.75;
} */
.cta-btn {
  font-size: 1rem;
  line-height: 1.5rem;
  font-weight: 900;
  padding: 10px 20px;
  background: #b22222;
  color: white;
}

  </style>
  