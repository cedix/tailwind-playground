<template>
  <section>
    <h1 class="flex justify-center text-xl font-bold">NUXTJS / Tailwind CSS Template</h1>
    <div class="px-8">
      <collapsible class="mt-8"/>
    </div>
  </section>
</template>

<script>
import Collapsible from "@/components/VCollapsible.vue";
export default {
  components: {
    Collapsible
  }
};
</script>

<style scoped>
</style>
