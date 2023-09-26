<!-- eslint-disable vue/first-attribute-linebreak -->
<template>
  <div class="w-full">
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24 pt-12">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-10 space-y-4 sm:space-y-6 px-6  sm:text-left">
        <div class="max-md:text-center max-sm:invisiblefi">
          <img :src="require('~/assets/img/logo/sl-logo-white.png')" class="w-[100px] xl:w-[150px]"
            alt="SoftwareGestionale Logo" />
          <h4 data-aos-once="true" data-aos-delay="300" class="hidden text-white sm:block">
            Fatturazione, contabilità, salari.
          </h4>
          <h1 id="indexMainText" data-aos-once="true"
            class="text-[2.5rem] mb-8 mt-8 text-white sm:text-4xl xl:text-5xl font-bold leading-tight sm:pr-8 xl:pr-10">
            Il software gestionale <br />
            per le PMI della svizzera italiana.
          </h1>
          <div data-aos-once="true" data-aos-delay="700"
            class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4 mt-2">
          </div>
            <a href="#"
              class="rounded-md  bg-white px-3.5 py-2.5 text-sm font-semibold text-sky-500 shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600">prova
              gratuitamente</a>
          </div>
        </div>
        <div class="hidden lg:block col-span-12 lg:col-span-6">
          <div class="w-full">
            <img data-aos-once="true" :src="require('~/assets/img/partner/cliente.png')" class="px-6  mt-4 max-w-[500px]"
              alt="" />
          </div>
        </div>
      </BaseSection>
    </section>

    <!-- Products Landing Section -->
    <LandingProductsLanding> </LandingProductsLanding>

    <!-- FAQ section -->
    <section class="w-full my-24">
      <BaseSection>
        <div data-aos="fade-left" data-aos-delay="150"
          class="text-center col-span-12 lg:col-span-8 lg:col-start-3 px-4 sm:px-6 mt-8">
          <h2 class="text-1xl sm:text-2xl font-semibold mb-20 sm:mb-12">
            Gestisci la tua azienda in modo semplice ed efficiente
          </h2>

          <ul class="shadow-box">
            <BaseAccordion v-for="(accordion, index) in accordions" :key="index" :accordion="accordion" />
          </ul>
        </div>
      </BaseSection>
    </section>

    <!-- Partners Break -->
    <div class="w-full bg-primary text-center">
      <!-- Hero section -->
      <section id="hero" class="w-full pb-2 text-center">
        <img class="margin-logo" :src="require('~/assets/img/startup.png')" />
      </section>
      <div>
        <h4 class="text-white text-3xl pb-16 font-black">
          SelectLine Good Start per il primo anno <br />
          ...gratuitamente
        </h4>
      </div>
    </div>

    <!-- Good Start Section -->
    <section class="w-full my-36">
      <BaseSection data-aos="fade-down">
        <div class="col-span-12 lg:col-span-7 md:m-auto">
          <div class="w-full sm:px-6 ">
            <img :src="require('~/assets/img/partner/goodstart.png')" class="w-[80%]" alt="" />
          </div>
        </div>
        <div class="col-span-12 lg:col-span-5 space-y-6 px-4 sm:px-6 mt-20">
          <h2 class="text-4xl font-semibold">
            La nostra <span class="text-header-gradient">offerta</span> per la vostra azienda
          </h2>
          <!-- <p class="paragraph">
            Subject to cardholder and rewards terms which will be available at
            application.
          </p> -->
          <ul class="space-y-4 sm:space-y-2">
            <LandingListItem
              content="Vi forniamo il software SelectLine per 1 anno senza alcun impegno. Contattateci nel corso dei primi 24 mesi dalla costituzione della vostra azienda e potrete utilizzare gratuitamente il software ERP per le PMI." />
            <LandingListItem
              content="Potete utilizzare l'intera gamma di funzionalità offerte dal programma SelectLine e i moduli Ordini, Contabilità e Salari senza alcuna restrizione."
              title="L’ERP per la vostra Start-up" />
            <LandingListItem
              content="Al termine del primo anno di utilizzo gratuito decidete, senza alcun impegno, se desiderate acquisire le licenze ufficiali che vi servono oppure no."
              title="Decidete voi se proseguire" />
            <LandingListItem
              content="Grazie a Goodstart, dopo la costituzione della vostra azienda, potrete concentrarvi completamente sull’attività operativa della vostra azienda."
              title="La nostra offerta per la vostra Start-up" />
          </ul>
        </div>
      </BaseSection>
      <LandingPricingLanding></LandingPricingLanding>
    </section>

    <!-- Partners Break -->
    <div class="w-full bg-primary text-center">
      <!-- Hero section -->
      <div class="py-32">
        <h4 class="text-white text-3xl font-black">
          Le aziende che hanno scelto SelectLine
        </h4>
      </div>
    </div>

    <!-- Partners section -->
    <section class="bg-partner relative max-w-full sm:mx-6 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full px-12 sm:px-0 py-8 flex flex-col items-center justify-center space-y-4 text-center">
        <div data-aos="fade-up" class="flex flex-wrap items-center justify-center gap-x-36 max-w-[70%]">
          <LandingPartnerImage v-for="img in [
            'autoaccessorio-removebg-preview.png',
            'paganini-removebg-preview.png',
            'battaglia.png',
            'vismara-removebg-preview.png',
            'biaggini-removebg-preview.png',
            'triacca-removebg-preview.png',
            'cortesi-removebg-preview.png',
          ]" :key="img" :img="img" class="max-w-[200px] partner-img" />
        </div>
      </div>
    </section>

    <!-- Partners Break -->
    <div class="w-full bg-primary text-center">
      <!-- Hero section -->
      <div class="text-center py-12">
        <h4 class="text-white text-3xl sm:text-4xl font-black">
          Mancanza di assistenza post vendita?
        </h4>
      </div>
      <div class="text-center">
        <h5 class="text-white px-2 text-2xl sm:text-3xl pb-16">
          Non con noi! Il nostro team esperto e competente ti affiancherà <br /> costantemente durante l'implementazione e
          l'utilizzo di SelectLine.
        </h5>
      </div>
    </div>

    <!-- Testimonials -->

    <!-- Partners Break -->
    <div class="w-full bg-white text-center">
      <!-- Hero section -->
      <div class="text-center py-12">
        <h4 class="text-primary text-md font-black pb-8">
          mail:
        </h4>
        <div>
          <a href="mailto:support@dpstudio.ch"
            class="rounded-md bg-primary px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600" >support@dpstudio.ch</a>
        </div>
      </div>
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
      selected: 0,
      dropdownConcurency: false,
      dropdownCrypto: false,
      accordions: [
        {
          title: "semplice",
          description:
            "Gestione degli ordini, contabilità finanziaria e salari saranno elaborabili in modo estremamente intuitivo e rapido. L'amministrazione della tua attività sarà un gioco da ragazzi.",
        },
        {
          title: "flessibile",
          description:
            "Gestione degli ordini, contabilità finanziaria e salari saranno elaborabili in modo estremamente intuitivo e rapido. L'amministrazione della tua attività sarà un gioco da ragazzi. ",
        },
        {
          title: "intersettoriale",
          description:
            "Gestione degli ordini, contabilità finanziaria e salari saranno elaborabili in modo estremamente intuitivo e rapido. L'amministrazione della tua attività sarà un gioco da ragazzi. ",
        },
      ],
      steps: [
        {
          img: "sign-up.png",
          title: "Sign Up",
          description:
            "Sign up for your free NEFA Wallet on web, iOS or Android and follow our easy process to set up your profile",
        },
        {
          img: "fund.png",
          title: "Fund",
          description:
            "Choose your preferred payment method such as bank transfer or credit card to top up your NEFA Wallet",
        },
        {
          img: "buy-crypto.png",
          title: "Buy Crypto",
          description:
            "Buy Bitcoin or Ethereum, then securely store it in your Wallet or send it on easily to your friends anywhere",
        },
      ],
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

.margin-logo {
  width: 200px;
  margin: auto;
  padding-top: 4rem;
}

</style>
