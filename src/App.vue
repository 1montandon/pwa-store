<script setup>
import ListagemProdutos from '@/components/ListagemProdutos.vue';
import MenuSuperior from './components/MenuSuperior.vue';''
import RodapeDesktop from './components/RodapeDesktop.vue';
import RodapeCell from './components/RodapeCell.vue';
import { useScreen } from '@/composables/screen';

const { browserWidth, deviceWidth, isMobile } = useScreen();

</script>

<template>
  <MenuSuperior/>
  <ListagemProdutos />
  <RodapeDesktop v-if="isMobile"/>
  <RodapeCell v-else/>
</template>