<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        

        <q-toolbar-title class="absolute-center">
          {{title}}
        </q-toolbar-title>

        
      </q-toolbar>
    </q-header>

   
   

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  computed: {
    title() {
      console.log(this.$route.fullPath);
      let currentPath = this.$route.fullPath;

      if (currentPath === '/') {
        return 'QuasarChat';
      } else if(currentPath === '/chat') {
        return 'Chat';
      } else if(currentPath === '/auth') {
        return 'Login';
      }
    }
  }
})
</script>
