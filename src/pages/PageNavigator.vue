<template>
  <v-container>
    <v-layout>
      <v-navigation-drawer :scrim="false" v-model="drawer" :location="`left`" expand-on-hover rail>
        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-note-edit" title="Marketing Material"
            @click="currentView = 'marketing_material'"></v-list-item>
          <v-list-item prepend-icon="mdi-calendar-clock" title="Marketing Campaign Plan"
            @click="currentView = 'marketing_campaign_plan'"></v-list-item>
          <v-list-item prepend-icon="mdi-film" title="Video Message"
            @click="currentView = 'video_message'"></v-list-item>
          <v-list-item prepend-icon="mdi-play-circle" title="Video Preview"
            @click="currentView = 'video_preview'"></v-list-item>
          <v-list-item prepend-icon="mdi-wrench-cog" title="Settings" @click="currentView = 'settings'"></v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-layout>
    <v-container>
        <Settings v-if="currentView == `settings`"></Settings>
    </v-container>
  </v-container>

</template>

<script setup>
import { ref, shallowRef } from 'vue';
import Settings from './Settings.vue';
const drawer = true
var currentView = shallowRef("mdi-note-edit");
</script>
