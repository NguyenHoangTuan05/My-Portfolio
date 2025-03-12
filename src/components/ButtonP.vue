<script setup>

import {Code,Eye} from "lucide-vue-next";

const props = defineProps({
  isEdit:Boolean,
  link:String
})
</script>

<template>
  <a class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link flex justify-center items-center"
     :href="props.link"> <Code v-if="props.isEdit" size="30" /><Eye v-else size="30" />
  </a>
</template>
