<!-- eslint-disable vue/first-attribute-linebreak -->
<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24 pt-12">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 space-y-4 sm:space-y-6 px-6 sm:text-left mt-auto">
          <img :src="require('~/assets/img/logo/sl-logo-white.png')" class="w-[100px] xl:w-[150px]"
            alt="SoftwareGestionale Logo" />
          <h1 data-aos-once="true"
            class="text-[2.5rem] text-white sm:text-4xl xl:text-5xl font-bold leading-tight sm:pr-8 xl:pr-10 ">
            SelectLine Supporto
          </h1>
        </div>
        <div class="hidden lg:block col-span-12 lg:col-span-6">
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/support.png')" class="mt-4 max-w-[500px]" alt="" />
          </div>
        </div>
      </BaseSection>
    </section>

    <!-- Main USP -->
    <section class="w-full my-24">
      <BaseSection data-aos="fade-down">
        <div class="col-span-12 lg:col-span-5 md:m-auto">
          <div class="w-full sm:px-6 mt-6">
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
        </div>
        <div class="col-span-12 lg:col-span-6 space-y-6 px-2 sm:px-6 mt-20 text-center">
          <ul>
            <li class="marker">
              <img :src="require('~/assets/img/sup1.png')" class="w-[20px] mr-2 inline">
              <a href="#"
                class="rounded-md bg-primary px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600 ml-8"
                style="color: white !important;">avvia assistenza remota</a>
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/sup2.png')" class="w-[20px] mr-2 inline">
              <a href="#"
                class="rounded-md bg-white ry px-3.5 py-2.5 text-sm font-semibold text-primary shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600 ml-8 text-center">
                <span class="w-[180px]" style="display: inline-block;">+41 839 00 00</span>
              </a>
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/sup3.png')" class="w-[20px] mr-2 inline">
              <a href="mailto:support@dpstudio.ch"
                class="rounded-md bg-primary ry px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600 ml-8 text-center">
                <span class="w-[180px]" style="display: inline-block;">support@dpstudio.ch</span>
              </a>
            </li>
          </ul>
        </div>
      </BaseSection>
      <LandingPricingLanding></LandingPricingLanding>
    </section>

    <!-- Products Landing Section -->
    <LandingProductsLanding> </LandingProductsLanding>


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
          title: 'Il nostro supporto al servizio della tua azienda', content: 'Nel processo di acquisto del software analizzeremo con te le reali esigenze della tua attività è fondamentale per trovare il giusto software gestionale: valuteremo insieme la migliore soluzione per ottenere il risultato desiderato. Abbiamo venticinque anni di esperienza nella distribuzione di software gestionali: siamo in grado di suggerirti i diversi aspetti da considerare nella fase di acquisto e di implementazione del programma.'
        },
        {
          title: 'Supporto prima, durante e dopo', content: 'Ti staremo accanto anche dopo aver installato il programma. Potrai sempre contare sul nostro supporto sia di persona che da remoto. Seguiremo l’attività della tua azienda con SelectLine passo dopo passo: se avrai bisogno di nuove funzionalità il nostro team tecnico potrà implementare nuove funzioni e/o strumenti ad hoc. In caso di problemi o domande potrai sempre contare sul nostro servizio di support, attento e competente, a tua disposizione all’indirizzo email support@dpstudio.ch.'
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

.margin-logo {
  width: 200px;
  margin: auto;
  padding-top: 4rem;
}
</style>
