<template>
  <dd>
    <div
      class="bg-white px-8 py-8 sm:pt-28 sm:pb-8 text-3xl font-semibold tracking-tight text-gray-900 sm:text-3xl text-center">
      La tua azienda a portata di click
    </div>
    <div
      class="bg-white py-2 font-semibold tracking-tight text-primary sm:text-lg text-center">
      scopri il catalogo >
    </div>
    <div class="bg-white pt-24 pb-4 sm:pt-32 px-2">
      <div class="mx-auto max-w-7xl px-6 lg:px-8 box-shadow-dpstudio">
        <dl class="flex flex-row justify-around">
          <div v-for="stat in stats" :key="stat.id" class="text-center w-24">
            <img :src="stat.image" class="max-w-[60px] m-auto my-4" />
            <dd class="text-primary">{{ stat.value }}</dd>
          </div>
        </dl>
      </div>
    </div>
    <LandingProductsComboLanding></LandingProductsComboLanding>
    <div class="bg-white py-4 sm:pt-2 sm:pb-2 text-lg tracking-tight text-gray-900 sm:text-lg text-center mt-8">
      A partire da 290.-
    </div>
    <div
      class="bg-white py-2 sm:pt-8 sm:pb-8 text-3xl font-semibold tracking-tight text-gray-900 sm:text-1xl text-center">
      <a href="#"
        class="rounded-md bg-primary px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600">prova
        gratuitamente
        </a>
    </div>
  </dd>
</template>

<script>
import ordiniImage from "../../assets/img/folder2.png"; // relative path to image
import contabilitaImage from "../../assets/img/calculator.png"; // relative path to image
import salariImage from "../../assets/img/people.png"; // relative path to image

export default {
  name: "ProductsLanding",
  data() {
    return {
      stats: [
        { value: "ordini", image: ordiniImage},
        { value: "contabilità", image: contabilitaImage },
        { value: "salari", image: salariImage },
      ],
    };
  },
};
</script>
<style scoped>
.box-shadow-dpstudio {
  border-radius: 1rem;
  box-shadow: rgba(145, 145, 145, 0.25) 0px 5px 5px, rgba(164, 164, 164, 0.22) 0px 10px 10px;
  border-top: 1px solid rgba(145, 145, 145, 0.25);
  padding: 2.5rem;
}
</style>
