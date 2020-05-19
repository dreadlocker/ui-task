<template>
  <div class="content-holder">
    <div class="content-header-1 absolutely-centered">{{contentHeader}}</div>
    <BaseContentWindow
      v-for="(window, index) in contentWindows"
      :key="index"
      :window="window"
      :index="index"
      :lastIndex="lastIndex"
    />
  </div>
</template>

<script>
import BaseContentWindow from '@/components/BaseContentWindow.vue'

export default {
  name: 'BaseHomePageContent',
  components: {
    BaseContentWindow,
  },
  props: {
    contentHeader: {
      type: String,
      required: true
    },
    contentWindows: {
      type: Array,
      required: true
    },
  },
  computed: {
    lastIndex() {
      return this.contentWindows.length - 1
    }
  }
}
</script>
