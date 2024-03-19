<template>
  <div>
    <!-- Mobile view -->
    <MobileView v-if="isMobile" />

    <!-- Desktop view -->
    <DesktopView v-else />
  </div>
</template>

<script>
import MobileView from "@/components/MobileView.vue";
import DesktopView from "@/components/DesktopView.vue";

export default {
  components: {
    MobileView,
    DesktopView,
  },
  data() {
    return {
      isMobile: window.innerWidth < 768, // 
    };
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.isMobile = window.innerWidth < 768; 
    },
  },
};
</script>
