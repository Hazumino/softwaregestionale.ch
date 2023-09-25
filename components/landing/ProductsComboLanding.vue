<template>
  <dd>
    <div class="bg-white py-2 sm:py-2">
      <div class="mx-auto max-w-7xl px-6 lg:px-8 box-shadow-dpstudio-small">
        <dl id="flexCombo" class="flex flex-row justify-around">
          <img :src="require('~/assets/img/partner/goodstart.png')" class="flexItem  h-[40px]"/>
          <img :src="require('~/assets/img/combo.png')" class="flexItem h-[25px]"/>
          <a href="#"
              class="rounded-md mb-2 bg-primary px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-white-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600">prova
              gratuitamente</a>
        </dl>
      </div>
    </div>
  </dd>
</template>

<script>
import ordiniImage from "../../assets/img/folder2.png"; // relative path to image
import contabilitaImage from "../../assets/img/calculator.png"; // relative path to image
import salariImage from "../../assets/img/people.png"; // relative path to image

export default {
  name: "ProductsComboLanding",
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
.box-shadow-dpstudio-small {
  border-radius: 1rem;
  box-shadow: rgba(145, 145, 145, 0.25) 0px 5px 5px, rgba(164, 164, 164, 0.22) 0px 10px 10px;
  padding: 1.5rem;
  border-top: 1px solid rgba(145, 145, 145, 0.25);
}
  #flexCombo
    {
    align-items:center;
  }
@media (max-width: 768px) {
  #flexCombo
    {
    flex-direction: column;
    align-items: center; /* Center the contents vertically */
    justify-content: center; /* Center the contents horizontally */
  }
  .flexItem
    {

    margin-bottom: 2rem;
  }
}



</style>
