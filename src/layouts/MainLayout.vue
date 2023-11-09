<template>
  <q-layout view="hHh Lpr lFf">
    <q-header elevated class="bg-orange">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <q-btn icon="mdi-logout" flat round padding="2px " />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-toolbar class="bg-primary" />
        <q-item class="bg-grey-3">
          <q-item-section>Lists</q-item-section>
          <q-item-section side>
            <q-btn icon="mdi-plus" flat round></q-btn>
          </q-item-section>
        </q-item>
        <q-item clickable>
          <q-item-section side>
            <q-icon name="mdi-shopping" color="grey-6" />
          </q-item-section>
          <q-item-section class="text-grey-9">
            Shopping List
          </q-item-section>
          <q-item-section side>
            12
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
/* import EssentialLink from 'components/EssentialLink.vue' */

export default defineComponent({
  name: 'MainLayout',
  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
