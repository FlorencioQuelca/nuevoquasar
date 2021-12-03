<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Admin </q-toolbar-title>

        <div>FONDO NACIONAL DE INVERSION PUBLICA Y SOCIAL</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> FPS-LAPAZ </q-item-label>
       
        <q-item clickable v-ripple to ="/">
          <q-item-section avatar>
            <q-icon color="teal" name="home" />
          </q-item-section>

          <q-item-section>Home</q-item-section>
        </q-item>
      
      <q-item clickable v-ripple to = "page1">
          <q-item-section avatar>
            <q-icon color="teal" name="person" />
          </q-item-section>

          <q-item-section>Page</q-item-section>
        </q-item>
      
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    // EssentialLink
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      //  essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
