<template>
  <v-app id="inspire">
    <v-stepper v-model="e6" vertical>
      <v-stepper-step :complete="e6 > 1" step="1">
        Instrucciones
        <small>para el llenado de la encuesta</small>
      </v-stepper-step>

      <v-stepper-content step="1">
        <instrucciones />
        <v-btn color="primary" @click="e6 = 2">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step :complete="e6 > 2" step="2">Datos generales</v-stepper-step>

      <v-stepper-content step="2">
        <datos-generales />
        <v-btn color="primary" @click="e6 = 3">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step :complete="e6 > 3" step="3">Antecendetes de atención</v-stepper-step>

      <v-stepper-content step="3">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 4">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="4" :complete="e6 > 4">Embarazo y parto</v-stepper-step>
      <v-stepper-content step="4">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 5">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="5" :complete="e6 > 5">Caracteristicas del desarrollo</v-stepper-step>
      <v-stepper-content step="5">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 6">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="6" :complete="e6 >6">Estado de salud</v-stepper-step>
      <v-stepper-content step="6">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 7">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="7" :complete="e6 > 7">Antecedentes familiares</v-stepper-step>
      <v-stepper-content step="7">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 8">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="8" :complete="e6 > 8">Habitos y autonomia</v-stepper-step>
      <v-stepper-content step="8">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 9">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>

      <v-stepper-step step="9" :complete="e6 > 9">Antecedentes educativos</v-stepper-step>
      <v-stepper-content step="9">
        <v-card color="grey lighten-1" class="mb-12" height="200px"></v-card>
        <v-btn color="primary" @click="e6 = 1">Continuar</v-btn>
        <v-btn text>Cancelar</v-btn>
      </v-stepper-content>
    </v-stepper>
  </v-app>
</template>
<script>
import Instrucciones from '~/components/steps/Instrucciones.vue'
import DatosGenerales from '~/components/steps/DatosGenerales.vue'

export default {
  components: {
    Instrucciones,
    DatosGenerales
  },
  data() {
    return {
      e6: 1,
      items: ['Item 1', 'Item 2', 'Item 3', 'Item 4']
    }
  }
}
</script>
