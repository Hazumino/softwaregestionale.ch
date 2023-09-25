
<template>
  <footer class="w-full mx-auto bg-[#004a7f]">

    <div class="w-full border-y border-[#DDDDDD]">
      <div class="grid xl:grid-cols-4 lg:grid-cols-2 md:grid-cols-2 sm:grid-cols-1">
        <div
          class="md:w-full lg:w-full w-full sm:w-1/2 xl:w-fit flex flex-col sm:flex-row sm:px-6 py-6 sm:py-12 sm:space-x-10 sm:border-r-0 border-[#DDDDDD]">
          <div class=" xl:block mb-6 sm:mb-0 p-4">
            <img :src="require('~/assets/img/logo/logo.png')" class="w-[240px]" alt="dp Logo" />
            <div class="mt-4 text-md text-white">
              softwaregestionale.ch è un dominio di dpstudio.ch sviluppato al fine di promuovere la suite selectline.ch ed
              i suoi prodotti di software gestionali per il mercato
              svizzera. La suite si compone di 5 moduli (ordini, contabilità, salari, start-up, supporto)
            </div>
          </div>
        </div>
        <div
          class="md:w-full lg:w-full lg:border-r w-full sm:w-1/2 xl:w-fit sm:px-16 py-6 sm:py-12 ml-8 md:ml-0 lg:ml:0  xl:border-r border-[#DDDDDD]">
          <ul class="space-y-4">
            <NavLink name="Ordini" url="/ordini" />
            <NavLink name="Contabilità" url="/contabilita" />
            <NavLink name="Salari" url="/salari" />
            <NavLink name="Startup" url="/startup" />
            <NavLink name="Supporto" url="/supporto" />
          </ul>
        </div>
        <div
          class="md:w-full md:border-t lg:w-full w-full sm:w-1/2 xl:w-fit sm:px-16 py-6 sm:py-12 border-t sm:border-t-0 sm:border-r-0 border-[#DDDDDD]">
        </div>
        <div
          class="md:w-full md:border-t lg:w-full sm:px-10 py-6 sm:py-12 w-full sm:w-1/2 xl:w-[22rem] space-y-4 sm:border-t border-[#DDDDDD]">

        </div>
      </div>
    </div>
    <div class="py-8 sm:py-4 text-center text-sm text-white hover:text-gray-900">
      &copy; Made with love by Northsouth UX SAGL.
    </div>
    <div id="footerFlex" class="bg-[#00B2FF] flex flex-row py-8 sm:py-4 text-left text-sm text-white hover:text-gray-900 items-center">
      <img data-aos-once="true" :src="require('~/assets/img/logodp.png')" class="mt-4 mb-4 w-[200px] flexItem" alt="" />
      <span class="flexItem font-bold ml-8 text-1xl">
        +41 81 839 00 00
      </span>
      <a href="mailto:support@dpstudio.ch"
            class="flexItem rounded-md bg-primary px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600 ml-8" style="color: white !important;">support@dpstudio.ch</a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'BaseFooter',
}
</script>
<style scoped>
a {
  color: blue
}

.abs {
  position: absolute;
  width: 500px;
  bottom: 0px;
  right: 0px;
}

@media (max-width: 768px) {

  #dpsLogo
    {
    display:none;
  }

  #footerFlex
    {
    padding-right:1rem;
    flex-direction: column;
  }

  .flexItem
    {
    margin-bottom:20px;
  }
}

