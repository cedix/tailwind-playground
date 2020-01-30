<template>
  <section>
    <h1 class="flex justify-center text-xl font-bold">NUXTJS / Tailwind CSS Playground</h1>
    <div class="px-8">
      <collapsible class="mt-8"/>
    </div>
    <div class="m-8 bg-gray-200 rounded p-4">
      <div class="flex mt-6 error-details">
        <!-- Full Class -->
        <div class="flex flex-col items-start">
          <span class="text-sm text-gray-600 field-label">Full Class</span>
          <span
            class="text-left field-value"
          >RETCODE=102 COMMAND=/product/pif/tibco/scripts/cft_send.sh QSAMR08 PATSCHH /product/pif/tibco/esb/data/pif/SEDSOC/POS/VALO/01/POSVALO01.20200127.0001.PROCESSING_VALID/OUTSAMPRO01-20200128085658769 940 OUTPUT=DIAG Interne: 200 / DIAG Protocolaire: (send_cft) CFTUTIL SEND IDF=QSAMR08,PART=PATSCHH,FNAME='/product/pif/tibco/esb/data/pif/SEDSOC/POS/VALO/01/POSVALO01.20200127.0001.PROCESSING_VALID/OUTSAMPRO01-20200128085658769',FLRECL=940,FRECFM=F Texte (lg ligne: 940, nb lignes: 314455) (IDT: DIAG Interne: 200 / DIAG Protocolaire:) ERROR=</span>
          <!-- <span>Short text</span> -->
        </div>

        <!-- Stack Trace -->
        <div class="flex flex-col items-end">
          <span class="text-sm text-gray-600">Stack Trace</span>
          <span class="field-value">Lorem ipsum</span>
        </div>
      </div>
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
.error-details {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 100px;
  grid-gap: 1em;
}

.field-value {
  word-break: break-all;
}
</style>
