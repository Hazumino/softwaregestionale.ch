<!-- eslint-disable vue/first-attribute-linebreak -->
<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24 pt-12">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 space-y-4 sm:space-y-6 px-6  sm:text-left mt-auto">
          <img :src="require('~/assets/img/logo/sl-logo-white.png')" class="w-[100px] xl:w-[150px]"
            alt="SoftwareGestionale Logo" />
          <h1 data-aos-once="true"
            class="text-[2.5rem] text-white sm:text-4xl xl:text-5xl font-bold leading-tight sm:pr-8 xl:pr-10 ">
            SelectLine Ordini
          </h1>
        </div>
        <div class="hidden lg:block col-span-12 lg:col-span-6">
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/ordini.png')" class="mt-4 max-w-[500px]" alt="" />
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
              Documenti di vendita e acquisto in un click
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Gestione articoli e magazzino
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Gestione dei prezzi con diversi listini e possibilità di ribasso
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Divise estere e lingue straniere
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Poste aperte e traffico dei pagamenti integrati
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Ordini di produzione
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Gestione di progetti e contratti
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Ordini di produzione
            </li>
            <li class="marker">
              <img :src="require('~/assets/img/li_item.png')" class="w-[20px] mr-2 inline">
              Report ed analisi aziendali a colpo d’occhio
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
      <LandingPricingLanding selected="ordini"></LandingPricingLanding>
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
        { title: 'Il cuore dell attività amministrativa', content: 'SelectLine Ordini ti permetterà di gestire in modo integrato tutti gli aspetti legati ad ordini e fatture: indirizzi di clienti e fornitori, articoli in vendita e loro descrizioni, prezzi e ribassi, documenti di acquisto e vendita, contratti, stoccaggio degli articoli prodotti, bolle di consegna, gestione del magazzino, inventariazione, traffico pagamenti in entrata ed uscita.' },
        { title: 'Modulare', content: 'Assieme al modulo Ordini avrai, inoltre, a disposizione soluzioni integrate come il modulo Cassa, il CRM o il modulo Mobile per garantire una maggiore completezza al tuo programma gestionale, secondo le esigenze specifiche della tua azienda.' },
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
