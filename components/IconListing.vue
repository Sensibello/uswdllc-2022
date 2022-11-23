<template>
     <section class="self-center flex flex-col flex-1 items-center justify-center" id="icons">
      <section class="">
        <div class="py-8 px-4 mx-auto max-w-screen-xl sm:py-16 lg:px-6">
          <div class="max-w-screen-md mb-8 lg:mb-16">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">
              {{mainTitle}}
            </h2>
            <p class="text-gray-500 sm:text-xl dark:text-gray-400">
              {{mainDescription}}
            </p>
            <p class="text-gray-500">
              {{mainAdditionalText}}
            </p>
          </div>
          <div class="space-y-8 md:grid md:grid-cols-1 lg:grid-cols-2 md:gap-12 md:space-y-0" >
            <div class="icon-parent-item" v-for="item in items" :key="item.title">
              <div
                class="
                  gray-bg-circle
                "
              >
                    <img
                        class="rounded-lg item-icon"
                        :src="require(`~/assets/images/icons/${item.icon}`)" 
                        alt=""
                    />
              </div>
              <h3 class="mb-2 text-xl font-bold dark:text-white">{{item.itemTitle}}</h3>
              <p class="text-gray-500">
                {{item.itemDescription}}
              </p>
             
            </div>
           
          </div>
        </div>
      </section>
    </section>
</template>



<script>
    export default {
      name: 'IconListing',
  
      props: {
        mainTitle: {
          type: String
        },
        mainDescription: {
            type: String
        },
        mainAdditionalText: {
          type: String
        },

        icon: {
          type: String
        },
        itemTitle: {
          type: String
        },
        itemDescription: {
          type: String
        },
        itemAdditionalDescription: {
          type: String
        },
  
        items: {
          type: Array
          
        }
      }
    }
</script>
    

<style lang="postcss" scoped>

#icons {
    background: #eee;
    width: 100%;
}
.item-icon {
    width: 100%;
    max-width: 40px;
    position: absolute;
    margin-left: 15px;
    margin-top: 15px;

}

.gray-bg-circle {
    background: #fff;
    border-radius: 100%;
    width: 70px;
    height: 70px;
    position: relative;
    margin-bottom: 15px;
}
  
</style>
    