<template>
  <ResearchInterests :researchInterests="user.researchInterests" />
  <Education :education="user.education" />
  <Work :work="user.work" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Education from './sections/Education.vue'
import { User } from '@/types/user'

export default defineComponent({
  props: {
    user: Object as () => User,
  },
  components: {
    Education,
  },
})
</script>

<style lang="scss" scoped>
@import '@/styles/index.scss';
</style>
