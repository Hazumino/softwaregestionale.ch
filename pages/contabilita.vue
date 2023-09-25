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
            SelectLine Contabilità
          </h1>
        </div>
        <div class="hidden lg:block col-span-12 lg:col-span-6">
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/contabilita.png')" class="mt-4 max-w-[500px]" alt="" />
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
        <div class="col-span-12 lg:col-span-6 space-y-6 px-2 sm:px-6 mt-20">
          <ul>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Registrazioni semplici, multiple
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Gestione debitori e creditori
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Registrazioni con lettore ottico QR
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Stampe analisi (bilancio, conto economico, estratti,…)
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Poste aperte e traffico dei pagamenti integrati
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Esportazioni in excel per ulteriori analisi
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Gestione di progetti e contratti
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Contabilità analitica
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Mandanti illimitati
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Numeri di serie e lotto
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Mandanti illimitati
            </li>
          </ul>
        </div>
      </BaseSection>
      <LandingPricingLanding selected="contabilita"></LandingPricingLanding>
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
        { title: 'Pianificazione economico-finanziaria', content: 'Quando si tratta di pianificare la liquidità o effettuare nuovi investimenti occorrono informazioni economico-aziendali affidabili per poter prendere decisioni fondate. Con SelectLine Contabilità a disposizione uno strumento professionale che ti fornirà in ogni momento le cifre e le statistiche necessarie, che siano raffronti con l’anno  precedente o con il budget stimato, oppure fotografie attuali della contabilità finanziaria o analitica.' },
        { title: 'Perfetto in combinazione con SelectLine Ordini SelectLine Salari', content: 'Il gestionale per la contabilità di SelectLine è particolarmente indicato per le PMI della Svizzera Italiana, perché, grazie alla sua semplicità. permette anche a collaboratori con minime conoscenze contabili di lavorare in modo efficiente e professionale tramite una breve istruzione. Il modulo Contabilità è perfetto se integrato con SelectLine Ordini e Salari e può essere ampliato ottimamente con il Modulo Poste Aperte che permette di gestire la contabilità debitori e creditori in maniera efficiente.' },
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

.margin-logo {
  width: 200px;
  margin: auto;
  padding-top: 4rem;
}
</style>
