<template>
  <div :class="['collapsible', 'rounded', isExpanded ? 'expanded' : '']">
    <div class="title bg-gray-700 text-gray-200 cursor-pointer" @click="toggleCollapsible">
      <div class="px-4 py-2">Title</div>
    </div>
    <div class="content bg-gray-600 text-gray-200">
      <div class="px-4 py-2">Content</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    expanded: {
      type: Boolean,
      default: false
    }
  },

  data() {
    return {
      isExpanded: this.expanded
    };
  },

  methods: {
    toggleCollapsible() {
      this.isExpanded = !this.isExpanded;
    }
  }
};
</script>

<style>
:root {
  --animation-duration: 0.5s;
}
</style>


<style scoped>
.collapsible {
  overflow: hidden;
}
.collapsible > .content {
  max-height: 0;
  transition: max-height var(--animation-duration) ease-in-out;
  overflow: hidden;
}
.collapsible.expanded > .content {
  max-height: 40px;
}
</style>
