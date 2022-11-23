<template>
  <div class="wrapper">
    <Header />
    <nuxt />
    <call-to-action :items="[
      {
        title: 'Ready to get started?',
        subtitle: 'Call US Window Door & More to get a free quote and start looking at what high quality solutions work for you, your home, and your budget.',
        buttonText: 'Call us today',
        buttonLink: 'tel:440-285-4357',
      }
    ]" />
    <Footer />
  </div>
</template>

<script>
import CallToAction from '~/components/CallToAction.vue'


export default {
  components: {
    CallToAction,
  }

}
</script>
