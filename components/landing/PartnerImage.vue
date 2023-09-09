<template>
  <div class="mt-8 py-16">
    <img :src="require(`~/assets/img/partner/${img}`)" class="lg:w-72 mx-auto" alt="" />
  </div>
</template>
<script>
export default {
  props: {
    img: {
      type: String,
      default: '',
    },
  },
}
</script>
