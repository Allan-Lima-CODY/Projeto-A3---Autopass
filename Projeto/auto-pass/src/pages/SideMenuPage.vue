<template>
  <div class="side-menu-container">
    <SideMenu class="side-menu round-border" />
    <SideText class="side-text-container" :route="getRoute()" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import SideMenu from 'src/components/SideMenu.vue';
import SideText from 'src/components/SideText.vue';
import '../css/side-menu.css';

export default defineComponent({
  name: 'SideMenuPage',
  components: {
    SideMenu,
    SideText,
  },
  methods: {
    getRoute() {
      return this.$route.path;
    },
  },
});
</script>
