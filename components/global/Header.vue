<template>
  <header class="w-full flex flex-wrap items-center justify-between">
      <div
        id="banner"
        tabindex="-1"
        class="
          flex
          gap-8
          justify-center
          items-center
          py-3
          px-4
          w-full
          bg-gray-50
          border border-b border-gray-200
          sm:items-center
          dark:border-gray-700
          lg:py-4
          bg-gray-800
        "
      >
        <p class="text-sm font-light text-white">Contact us today to get a free estimate!</p>
        <a
          class="flex items-center hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm cta-button"
          href="tel:440-285-4357"
        >
          Call us now
        </a>
      </div>
  <div
    class="w-full"
    :class="{ 'absolute w-full h-screen toppy left-0': menu }"
  >
    <div class="mobiley w-full justify-between  md:mx-auto flex flex-wrap">
      <div class="w-auto p-3">
        <!-- Title -->
        <a href="/" class="flex items-center">
            <img src="~/assets/images/logo.png" class="mr-3 logo-img" alt="USWDLLC Logo" />
            <span class="sr-only">USWDLLC </span>
        </a>
        <!-- Icon -->
       
      </div>
      <!-- Desktop nav list -->
      <nav class="hidden lg:block">
        <ul class="flex">
          <li
            v-for="(item, index) in items"
            :key="index"
          >
            <a
              :href="item.href"
              class="hover:underline p-6 block"
            >
              {{ item.title }}
            </a>
          </li>
        </ul>
      </nav>
      <!-- Toggle menu mobile icon -->
        <div
          class="toggler ml-auto lg:hidden p-6"
          @click="menu = !menu"
        >
        <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
        </div>
      </div>
      <!-- Mobile nav list -->
      <nav v-show="menu" class="w-full dropping">
        <ul class="flex flex-col text-center">
        <li
          v-for="(item, index) in items"
          :key="index"
        >
          <a
            :href="item.href"
            class="bg-white p-6 block"
          >
            {{ item.title }}
          </a>
        </li>
      </ul>
    </nav>
  </div>
  </header>

</template>


<script>
export default {
  data() {
    return {
      menu: false,
      items: [
        {
          title: 'Home',
          href: '/'
        },
        {
          title: 'About',
          href: '/about'
        },
        {
          title: 'Services',
          href: '/services'
        },
        {
          title: 'Our Work',
          href: '/our-work'
        },
        {
          title: 'Provia Portal',
          href: '/provia-portal'
        },
        {
          title: 'Contact',
          href: '/contact'
        }
      ]
    }
  }
}
</script>

<style lang="postcss" scoped>

nav {
  li:last-child {
    background: #b22222;
    padding: 9px 18px;
    color: white;
    border-radius: 5px;
  }
}
.toggler {
  background: #eee;
}

.logo-img {
  width: 100%;
  max-width: 390px;
}
.mobiley {
  background: #fff;
  background: #fff;
  box-shadow: 9px 3px 4px #eee;
}

.toppy {
  top: 65px;
}

@media (max-width: 600px) {
  .logo-img {
  width: 100%;
  max-width: 290px;
}
  .mobiley {
    border-bottom: solid 2px #2C3A57;
  }

  .logo-img {
    width: 100%;
    max-width: 290px;
  }

  .dropping {
    box-shadow: 10px 10px 5px #ccc;
      ul {
        li {
          border-bottom: 1px solid #eee;
        }
      }
  }
}

</style>