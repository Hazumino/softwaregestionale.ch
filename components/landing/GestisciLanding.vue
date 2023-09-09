<template>
  <dd>
    <div
      class="bg-white py-8 sm:pt-28 sm:pb-8 text-3xl font-semibold tracking-tight text-gray-900 sm:text-3xl text-center">
      La tua azienda a portata di click
    </div>
    <div class="bg-white py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <dl class="grid grid-cols-1 gap-x-8 gap-y-16 text-center lg:grid-cols-3">
          <div v-for="stat in stats" :key="stat.id" class="mx-auto flex max-w-xs flex-col gap-y-4">
            <dt class="text-base leading-7 text-gray-600">{{ stat.name }}</dt>
            <dd class="order-first text-3xl font-semibold tracking-tight text-gray-900 sm:text-5xl">{{ stat.value }}</dd>
          </div>
        </dl>
      </div>
    </div>
    <div class="bg-white py-8 sm:pt-8 sm:pb-2 text-lg tracking-tight text-gray-900 sm:text-lg text-center">
      A partire da 290.-
    </div>
    <div
      class="bg-white py-2 sm:pt-8 sm:pb-8 text-3xl font-semibold tracking-tight text-gray-900 sm:text-1xl text-center">
      <a href="#"
        class="rounded-md bg-sky-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-sky-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white-600">prova
        gratuitamente</a>
    </div>
  </dd>
</template>

<script>
export default {
  name: 'GestisciLanding',
  data() {
    return {
      stats: [
        { id: 1, name: 'Transactions every 24 hours', value: 'ordini' },
        { id: 2, name: 'Assets under holding', value: 'contabilità' },
        { id: 3, name: 'New users annually', value: 'salari' },
      ]
    }
  }
}
</script>
