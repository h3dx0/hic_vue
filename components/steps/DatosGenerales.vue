<template>
  <div>
    <v-form v-model="valid" class="mb-5">
      <v-row>
        <v-col cols="12" md="3">
          <v-text-field v-model="firstname" :rules="nameRules" label="Nombre" required></v-text-field>
        </v-col>

        <v-col cols="12" md="3">
          <v-text-field v-model="lastname" :rules="nameRules" label="Apellido paterno" required></v-text-field>
        </v-col>
        <v-col cols="12" md="3">
          <v-text-field v-model="lastname" :rules="nameRules" label="Apellido materno" required></v-text-field>
        </v-col>

        <v-col cols="12" md="3">
          <v-text-field v-model="email" :rules="emailRules" label="Fecha Nacimiento" required></v-text-field>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="3">
          <v-select v-model="select" :items="items" label="Sexo" data-vv-name="select" required></v-select>
        </v-col>
        <v-col cols="12" md="3">
          <v-select v-model="select" :items="items" label="Edad" data-vv-name="select" required></v-select>
        </v-col>
        <v-col cols="12" md="3">
          <v-select v-model="select" :items="items" label="Ciudad" data-vv-name="select" required></v-select>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="12">
          <div>
            ¿Cuál es el motivo por el qué ha asistido usted a nuestra institución? En caso de haber sido remitido
            por algún
            especialista, refiera su nombre y el motivo por el cual lo remite. Aclare además que espera obtener
            como resultado del
            presente proceso evaluativo.
          </div>
        </v-col>
      </v-row>
    </v-form>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
</style>