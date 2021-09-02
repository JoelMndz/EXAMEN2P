<template>
   <h1> Vehiculos </h1> 
    <FormV />
</template>

<script>
import FormV from './FormV.vue'
import {provide, reactive, ref} from 'vue'

export default {
  name: 'Vehiculo',
  components: {
    FormV
  },
  setup(){
    const vehiculos = ref([]);
    const vehiculo = reactive({
      nombre:'',
      placa:'',
      espacio:'',
      numeroTicket:'',
      horas:0,
      costo:0
    })
    provide('vehiculo',vehiculo);
    provide('vehiculos', vehiculos);
  }
}
</script>

