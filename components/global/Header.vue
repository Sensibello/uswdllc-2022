<template>
  <header class="w-full flex flex-wrap items-center justify-between">
    <div
      id="banner"
      tabindex="-1"
      class="
        flex
        z-50
        gap-8
        justify-center
        items-start
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

    <!-- Navbar -->
    <nav
      class="
        navbar navbar-expand-lg
        shadow-md
        py-2
        px-6
        bg-white
        relative
        flex
        items-center
        w-full
        justify-between
        scrim-bg
        fixed
        z-40
        top-0
        inset-x-0
        pt-3
        px-3
      "
      aria-label="Main Menu"
    >
      <div class="px-6 w-full flex flex-wrap items-center justify-between">
        <a
          class="flex items-center text-gray-900 hover:text-gray-900 focus:text-gray-900 mt-2 lg:mt-0 mr-1 logo-link"
          href="#"
        >
          <img src="~/assets/images/logo.png" class="logo-img" alt="" loading="lazy" />
        </a>

        <div class="flex items-center">
          <button
            class="
              navbar-toggler
              border-0
              py-3
              lg:hidden
              leading-none
              text-xl
              bg-transparent
              text-gray-600
              hover:text-gray-700
              focus:text-gray-700
              transition-shadow
              duration-150
              ease-in-out
              mr-2
            "
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContentY"
            aria-controls="navbarSupportedContentY"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <svg
              aria-hidden="true"
              focusable="false"
              data-prefix="fas"
              class="w-5"
              role="img"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 448 512"
            >
              <path
                fill="currentColor"
                d="M16 132h416c8.837 0 16-7.163 16-16V76c0-8.837-7.163-16-16-16H16C7.163 60 0 67.163 0 76v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16z"
              ></path>
            </svg>
          </button>
        </div>
        <div class="navbar-collapse collapse grow items-center" id="navbarSupportedContentY">
          <ul class="navbar-nav mr-auto lg:flex lg:flex-row">
            <li class="nav-item">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  text-gray-600
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                "
                to="/home"
                >Home</nuxt-link
              >
            </li>
            <li class="nav-item">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  text-gray-600
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                "
                to="/services"
                >Services</nuxt-link
              >
            </li>
            <li class="nav-item">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  text-gray-600
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                "
                to="/about"
                >Who We Are</nuxt-link
              >
            </li>
            <li class="nav-item mb-2 lg:mb-0">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  text-gray-600
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                "
                to="/projects"
                >Our Work</nuxt-link
              >
            </li>
            <li class="nav-item mb-2 lg:mb-0">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  text-gray-600
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                "
                to="/provia-portal"
                >Provia Portal</nuxt-link
              >
            </li>
            <li class="nav-item mb-2 lg:mb-0">
              <nuxt-link
                class="
                  nav-link
                  block
                  pr-2
                  lg:px-2
                  py-2
                  hover:text-gray-700
                  focus:text-gray-700
                  transition
                  duration-150
                  ease-in-out
                  cta-button
                  rounded-lg
                "
                to="/contact"
                >Contact</nuxt-link
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- Navbar -->
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
.scrim-bg {
}
.nuxt-link-exact-active {
  @apply text-gray-200 border-gray-400 bg-gray-800 bg-opacity-25 cursor-default;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
      background: linear-gradient(to bottom, #e5e7eb, cubic-bezier(0.15, 0, 0.45, 1), transparent);
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-700 border-gray-600 bg-gray-100;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn2 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
