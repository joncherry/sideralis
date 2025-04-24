<template>
    <v-container>
        <v-row justify="center">
            <v-card class="ma-2 pa-2">
                <v-btn icon="mdi-invert-colors" @click="toggleTheme"></v-btn>
                <v-label>Light Theme</v-label>
            </v-card>
        </v-row>

    </v-container>
</template>

<script setup>
import { useTheme } from 'vuetify'

const theme = useTheme()

function toggleTheme() {
    theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}
</script>