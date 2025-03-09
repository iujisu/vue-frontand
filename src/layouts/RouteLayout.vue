<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="home" aria-label="home" @click="goHome" />
        <q-toolbar-title> 신규 App </q-toolbar-title>

        <div>app v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
<script setup>
import { useRouter } from "vue-router";
const router = useRouter();
const goHome = () => {
  router.push("/");
};
</script>
