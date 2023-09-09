<template>
  <li class="space-y-2">
    <span class="font-bold mb-4">{{ title }}</span>
    <div class="flex items-center space-x-2">
      <span>{{ content }}</span>
    </div>
    <slot></slot>
  </li>
</template>
<script>
export default {
  name: 'LandingListItem',
  props: {
    title: {
      type: String,
      default: '',
    },
    content: {
      type: String,
      default: '',
    },
  },
}
</script>
