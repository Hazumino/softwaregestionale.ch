<!-- eslint-disable vue/first-attribute-linebreak -->
<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24 pt-12">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 space-y-4 sm:space-y-6 px-6 sm:text-left mt-auto">
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/startup.png')" class="mt-4 max-w-[500px]" alt="" />
          </div>
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/partner/goodstart.png')"
              class="w-full sm:w-80 md:w-96 lg:w-4/5 xl:w-3/4 filter-white " alt="" />
          </div>
        </div>
        <div class="hidden sm:block col-span-12 lg:col-span-6">

        </div>
      </BaseSection>
    </section>

    <LandingProductsComboLanding class="mt-8"></LandingProductsComboLanding>

    <!-- Main USP -->
    <section class="w-full my-24">
      <BaseSection data-aos="fade-down">
        <div class="col-span-12 lg:col-span-5 md:m-auto">
          <div class="w-full sm:px-6 mt-6">
            <img data-aos-once="true" :src="require('~/assets/img/speciale.png')" class="mt-4 mb-8 max-w-[400px]"
              alt="" />
            <h2 class="text-1xl font-semibold mb-4">
              {{ text[0].title }}
            </h2>
            <LandingListItem :content="text[0].content" />
          </div>
          <div class="w-full sm:px-6 mt-6">
            <h2 class="text-1xl font-semibold mb-4">
              {{ text[1].title }}
            </h2>
            <LandingListItem :content="text[1].content" />
          </div>
          <div class="w-full sm:px-6 mt-6">
            <h2 class="text-1xl font-semibold mb-4">
              {{ text[2].title }}
            </h2>
            <LandingListItem :content="text[2].content" />
          </div>
          <div class="w-full sm:px-6 mt-6">
            <h2 class="text-1xl font-semibold mb-4">
              {{ text[3].title }}
            </h2>
            <LandingListItem :content="text[3].content" />
          </div>
        </div>
        <div class="col-span-12 lg:col-span-6 space-y-6 px-2 sm:px-6 mt-20">
          <img :src="require('~/assets/img/startupimg.png')" class="mr-2 inline">
        </div>
      </BaseSection>
      <LandingPricingLanding></LandingPricingLanding>
    </section>

    <!-- Products Landing Section -->
    <LandingProductsLanding> </LandingProductsLanding>

    <!-- Testimonials -->


    <div class="text-center">
        <h5 class="text-black text-2xl pb-16">
          ”SelectLine Goodstart ci ha davvero aiutato ad avviare la nostra nuova attività alla grande.<br />
          Abbiamo potuto concentrarci pienamente sulle nostre competenze principali.”
        </h5>
      </div>
      <div class="text-center">
        <h5 class="text-black text-2xl pb-16 font-thin pt-8">
          Rosemarie Zucca<br />
          Responsabile amministrazione SET Steril Expert Ticino
        </h5>
      </div>
      <div class="text-center pb-16">
        <img :src="require('~/assets/img/zucca.png')" class="w-[450px] m-auto -mt-2" alt="Ciente testimonial" />
      </div>

    <div class="w-full my-10 flex justify-center">
      <a v-smooth-scroll data-aos="flip-down" data-aos-delay="150" href="#navbar"
        class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700">
        <span>Torna su</span>
        <ArrowUpIcon :size="20" />
      </a>
    </div>
  </div>
</template>

<script>
import aosMixin from "@/mixins/aos";
export default {
  name: "IndexPage",
  mixins: [aosMixin],
  data() {
    return {
      text: [
        {
          title: 'La nostra offerta per la vostra azienda', content: 'Vi forniamo il software SelectLine per un anno senza alcun impegno. Contattateci nel corso dei primi 24 mesi dalla costituzione della vostra azienda e potrete utilizzare gratuitamente il software ERP per le PMI.'
        },
        {
          title: 'L’ERP per la vostra Start-up', content: 'Potete utilizzare l intera gamma di funzionalità offerte dal programma SelectLine e i moduli Ordini, Contabilità e Salari senza alcuna restrizione.'
        },
        {
          title: 'Decidi tu se proseguire', content: 'Al termine del primo anno di utilizzo gratuito decidete, senza alcun impegno, se desiderate acquisire le licenze ufficiali che vi servono oppure no.'
        },
        {
          title: 'La nostra offerta per la vostra Start-up', content: 'Grazie a Goodstart, dopo la costituzione della vostra azienda, potrete concentrarvi completamente sull’attività operativa della vostra azienda.'
        },
      ]
    };
  },
  head() {
    return {
      script: [
        {
          hid: 'cookiebot', body: 'true',
          id: 'Cookiebot', src: 'https://consent.cookiebot.com/uc.js', 'data-cbid': 'cb8de957-083e-4d32-a684-60677e492177', 'data-blockingmode': 'auto', type: 'text/javascript'

        }
      ],
    }
  },
};
</script>
<style scoped>
#hero {
  background: #0194d4;
}

.text-header-gradient {
  background: rgb(57, 132, 244);
  background: linear-gradient(169.4deg,
      #3984f4 -6.01%,
      #0cd3ff 36.87%,
      #2f7cf0 78.04%,
      #0e65e8 103.77%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.bg-partner {
  background: white;
  background-size: cover;
  background-position: center;
}

.partner-img:last-child {
  max-width: 300px;
}

.max-h-0 {
  max-height: 0;
}

li {
  list-style: none !important;
  margin-top: 20px;
}

li:first-child {
  margin-top: 0px;
}

.marker {
  margin-top: 4rem;
}

.filter-white {
  filter: brightness(0) invert(1);
}

.margin-logo {
  width: 200px;
  margin: auto;
  padding-top: 4rem;
}</style>
