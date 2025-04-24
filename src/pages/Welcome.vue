<template>
    <v-row justify="center">
        <h1 text-horizontal-align="center">Sideralis</h1>
    </v-row>
    <v-row justify="center">
        <p>A tool that generates marketing for social media</p>
    </v-row>
    <v-row>
        <v-text-field
            v-model="activationKey"
            label="Activation Key"
            hint="activation keys can be purchased at store.{put store address here}"
            prependIcon="mdi-key-chain"
            required
          ></v-text-field>
    </v-row>
</template>