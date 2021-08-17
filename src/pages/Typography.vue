<template>
  <q-page class="flex column q-pa-md">
    <!-- <h1>Typography</h1> -->
    <span class="text-h1">HeadLine 1</span>
    <span class="text-h2">HeadLine 2</span>
    <span class="text-h3">HeadLine 3</span>
    <span class="text-h4">HeadLine 4</span>
    <span class="text-h5">HeadLine 5</span>
    <span class="text-h6">HeadLine 6</span>

    <q-separator />

    <span class="text-subtitle1">Subtitulo 1</span>
    <span class="text-subtitle2">Subtitulo 2</span>

    <q-separator />
    <p class="text-body1">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
      voluptate ipsum explicabo quod! Repellendus provident nulla vel corrupti,
      porro aspernatur pariatur libero recusandae totam modi, fuga eveniet
      temporibus dolore quaerat.S
    </p>
    <p class="text-body2">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae
      voluptate ipsum explicabo quod! Repellendus provident nulla vel corrupti,
      porro aspernatur pariatur libero recusandae totam modi, fuga eveniet
      temporibus dolore quaerat.S
    </p>

    <q-separator />

    <span class="text-weight-thin"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >
    <span class="text-weight-light"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >
    <span class="text-weight-regular"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >
    <span class="text-weight-medium"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >
    <span class="text-weight-bold"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >
    <span class="text-weight-bolder"
      >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim, dolore
      reiciendis. Assumenda dolore, odit provident repellat ut hic
      expedita?</span
    >

    <q-btn 
      color="primary"
      :label=" sideMenuOpen ? 'Cerrar menú lateral' : 'Abrir menú lateral'"
      class="q-mt-md"
      @click="toggleSideMenu"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import useUI from '../composables/useUI'

export default defineComponent({
  name: "Typography",
  setup(){
    const { sideMenuOpen, toggleSideMenu } = useUI()

    return {
      sideMenuOpen,
      toggleSideMenu
    }
  }
});
</script>
