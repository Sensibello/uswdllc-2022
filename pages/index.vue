<template>
  <main>

    <hero-section :items="[
      {
        title: 'US Window Door & More',
        subhead: 'Serving Northeast Ohio for over 60 years. Family owned, locally operated.',
        text: 'We offer the most efficient and high quality replacement windows, new windows, siding, doors, and roofing.',
        buttonText: 'See our work',
        buttonLink: '/projects',
        photo: 'provia-windows/porch-window.jpeg',
      }
    ]" />


    <icon-listing 
      mainTitle="Undivided Responsibility" 
      mainDescription="What does undivided responsibility mean? It means that here at US Window Door & More when you buy replacement windows, entry doors or any other product from us and we install it, we guarantee your satisfaction."
      mainAdditionalText="If there are ANY problems down the road you only need to make one phone call to make it right – call US. We won’t hear your complaint and then ask you to call the manufacturer. We don’t want you to have to take care of the issue. We stand by our products and service and will bear the responsibility of quality performance."

      :items="[
        {
          icon: 'window.svg',
          itemTitle:'Provia Replacement Windows',
          itemDescription:'ProVia replacement windows carry the most efficient rating from energy star premium quality at fair prices. We are a direct seller for ProVia windows in Northeast Ohio, so we can guarantee you the best price with a seamless installation. We offer a wide range of premium windows, so call us today to schedule a consultation at our showroom in Chardon, Ohio to see your options.',
        },
        {
          icon: 'door.svg',
          itemTitle:'Doors',
          itemDescription:'We offer beautiful, quality and affordable wood, steel and fiberglass entry doors. There are multiple brands and price points to choose from (ProVia, Polaris, and Pella) which will cater to your specific design needs, custom requirements and budget concerns.',
        },
        {
          icon: 'house.svg',
          itemTitle:'Siding',
          itemDescription:'We carry all the major siding manufactures. We give you the freedom to choose the brand and style that distinguishes your unique tastes. We offer various types of vinyl siding, such as ship lap, lap, vertical, composite, and cellular PVC. The exterior of your home says something about who you are – express it!',
        },
        {
          icon: 'roof.svg',
          itemTitle:'Roofing',
          itemDescription:'We proudly offer Owens Corning roofing products which are the highest rated roofing materials on the market. OC manufactures roofing shingles with the upmost quality for peak performance. A number of shingle styles are available, each carrying their own traits and qualities.',
        }
      ]" />


    <text-with-image :items="[
      {
        title: 'About Us',
        paragraphOne: 'Our company is a third generation residential home improvement contractor. My grandfather, Lester Sensibello, started contracting in the 1930s. For over 60 years we have provided quality service to our customers in sticking to the adage of my grandfather who used to say, “Usa realla good stuff — put in realla good –and don’ta charga too mucha!”',
        paragraphTwo: 'We pride ourselves of being family owned and operated, serving our local communities in Northeast Ohio with the best solutions at affordable prices.',
        buttonText: 'Learn more about us',
        buttonLink: '/about',
        photoOne: 'dave.jpeg',
        photoTwo: 'warehouse.jpeg',
      }
    ]" />


    <testimonials :items="[
      {
        title: 'Could not have had a better experience!',
        text: 'Getting new windows for the whole house was quite a scary experience for me, however, Dave, the owner, was very patient, helpful and knowledgeable . He quickly made me feel at ease. They were very competitively priced and I believe the quality of the installation far exceeds their competition.',
        additionalText: 'His son Nick is a perfectionist and very detail orientated. He and Derrick worked hard, skillfully and respectfully. They were very neat and left no trace behind. We will happily recommend them. We are extremely satisfied with our new Windows!',
        name: 'Lisa L',
      },
      {
        title: 'Dave and his crew were AMAZING!',
        text: 'The Provia windows and doors are the best! Wish we would have done it years ago! Very professional and friendly. We have had several home improvement projects done and this company is the best by FAR! When they were done, it was like they were never there! They worked efficiently and effectively , getting the job done in a timely manner all with no mess!',
        additionalText: 'We are very happy with our new windows and door…looking forward to doing more doors in the near future! Thanks Dave and your whole team!',
        name: 'Jodi H.',
      },
      {
        title: 'I could not have been happier with this company and the job they did for me.',
        text: 'From the quality of the windows & the fairness of the price, to the hard working and professional installers. Nick went above and beyond to fix a water problem we discovered on install day. Can’t thank him enough for all he did. ',
        additionalText: 'Would highly recommend this company.',
        name: 'Stacey R.',
      },
      {
        title: 'Service was impeccable.',
        text: 'I used Dave at US windows for a full house set of windows and a couple doors. Price was competitive, windows and doors were superior products, and service was impeccable. The installers were courteous, fast, clean, and knowledgeable. ',
        additionalText: 'I have nothing but glowing things to say about US windows and the staff!',
        name: 'John K.',
      }
    ]" />

   
    <section>
      <!-- <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">Latest blog post</h3> -->
      <!-- <posts post-type="blog" :amount="1" /> -->
    </section>
  </main>
</template>

<script>
import CallToAction from '~/components/CallToAction.vue'
import Testimonials from '~/components/Testimonials.vue'
import TextWithImage from '~/components/TextWithImage.vue'
import IconListing from '~/components/IconListing.vue'
import HeroSection from '~/components/HeroSection.vue'

export default {
  components: {
    CallToAction,
    Testimonials,
    TextWithImage,
    IconListing,
    HeroSection
  }

}
</script>
