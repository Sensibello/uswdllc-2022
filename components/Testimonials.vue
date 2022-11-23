<template>
    <section class="bg-white dark:bg-gray-900">
        <div class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 lg:px-6">
        <div class="mx-auto max-w-screen-sm">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">Testimonials</h2>
            <p class="mb-8 font-light text-gray-500 lg:mb-16 sm:text-xl dark:text-gray-400">
            Don't just take our word for it -- see what our customers have to say about working with US Window Door &
            More.
            </p>
        </div>

        <div class="grid mb-8 lg:mb-12 lg:grid-cols-2">
            <figure class="testimonial-item flex flex-col justify-center items-center p-8 text-center bg-gray-50 md:p-12" v-for="item in items" :key="item.title">
            <blockquote class="mx-auto mb-8 max-w-2xl text-gray-500 dark:text-gray-400">
                <h3 class="text-lg font-bold text-gray-900 dark:text-white">{{item.title}}</h3>
                <p class="my-4">
                {{item.text}}
                </p>
                <p class="my-4">
                {{item.additionalText}}
                </p>
            </blockquote>
            <figcaption class="flex justify-center items-center space-x-3">
                <div class="space-y-0.5 font-medium dark:text-white text-left">
                <p>
                    <em><strong>{{item.name}}</strong></em>
                </p>
                </div>
            </figcaption>
            </figure>
            
            </div>
        </div>
    </section>
</template>



<script>
    export default {
      name: 'Testimonials',
  
      props: {
        title: {
          type: String
        },
        text: {
          type: String
        },
        additionalText: {
          type: String
        },
        name: {
          type: String
        },
  
        items: {
          type: Array
        }
      }
    }
</script>
    

<style lang="postcss" scoped>
.testimonial-item {
  border-left: 12px solid var(--color-red);
  margin: 10px;
}

  
    </style>
    