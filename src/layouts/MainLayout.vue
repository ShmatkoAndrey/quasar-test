<template>
    <q-layout view="hHh LpR fFr">

      <q-header elevated class="bg-primary text-white">
        <q-toolbar>
          <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

          <q-toolbar-title>
            <q-avatar>
              <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
            </q-avatar>
            Title
          </q-toolbar-title>
        </q-toolbar>
      </q-header>

      <q-drawer show-if-above v-model="leftDrawerOpen" side="left">
        <user-sidebar />
      </q-drawer>

      <q-page-container>
        <router-view />
      </q-page-container>

    </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import UserSidebar from 'src/components/common/UserSidebar.vue'

const leftDrawerOpen = ref(false)
const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
