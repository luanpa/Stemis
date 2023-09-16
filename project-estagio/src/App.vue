<template>

<v-app>
<v-navigation-drawer v-model="isDrawerOpen">
  <v-list>
    <v-list-subheader>Menu</v-list-subheader>
    <v-list-item prepend-icon="mdi-home">Home</v-list-item>
    <v-list-item prepend-icon="mdi-star">Lugares mais visitados </v-list-item>
    <v-list-item prepend-icon="mdi-pizza">Restaurantes mais visitados </v-list-item>
    <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>
    <v-list-item prepend-icon="mdi-account-arrow-right">Sair</v-list-item>



   </v-list>

</v-navigation-drawer>

<v-app-bar flat class="border-b">
  <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen">

  </v-app-bar-nav-icon>
  <v-btn icon="mdi-heart"></v-btn>

    <v-btn icon="mdi-magnify"></v-btn>

    <v-btn icon="mdi-dots-vertical"></v-btn>
  <v-app-bar-title class="center">Projeto Stemis </v-app-bar-title>


  <v-avatar>
      <v-img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      ></v-img>
    </v-avatar>

</v-app-bar>



  <v-main>
  <v-container>
    <v-btn color="primary" >Theme Dark ou Light</v-btn>
    <h1>Dashboard</h1>

    <v-card flat class="border mb-4">
      <div class="d-flex justify-space-between">
        <v-card-title>Deixe Seu Feedback</v-card-title>

        <v-card-title>
        <v-btn variant="tonal">Criar Conta</v-btn>
        </v-card-title>
      </div>


    <v-table density="compact">
      <thead>
        <tr>
          <th>Parque da Lajinha</th>
          <th>Museu Mariano </th>
          <th>Parque Halfeld</th>
          <th>Jardim Botânico da UFJF</th>
        </tr>
      </thead>
          <tbody>
            <tr>
              <td > <v-btn variant="tonal" color="primary" icon="mdi-thumb-up"></v-btn></td>
              <td > <v-btn variant="tonal" color="primary" icon="mdi-thumb-up"></v-btn></td>
             <td > <v-btn variant="tonal" color="primary" icon="mdi-thumb-up"></v-btn></td>
             <td > <v-btn variant="tonal" color="primary" icon="mdi-thumb-up"></v-btn></td>
            </tr>
            <tr>
              <td > <v-btn variant="tonal" color="red" icon="mdi-thumb-down"></v-btn></td>
              <td > <v-btn variant="tonal" color="red" icon="mdi-thumb-down"></v-btn></td>
             <td > <v-btn variant="tonal" color="red" icon="mdi-thumb-down"></v-btn></td>
             <td > <v-btn variant="tonal" color="red" icon="mdi-thumb-down"></v-btn></td>

            </tr>
            <tr>
              <td> <v-btn variant="tonal" color="primary">Reporte o acontecido</v-btn></td>
              <td> <v-btn variant="tonal" color="primary">Reporte o acontecido</v-btn></td>
              <td> <v-btn variant="tonal" color="primary">Reporte o acontecido</v-btn></td>
              <td> <v-btn variant="tonal" color="primary">Reporte o acontecido</v-btn></td>
            </tr>


          </tbody>
        </v-table>
      </v-card>



   <v-row>


    <v-col cols="12" md="4" lg="3">
      <v-card >
        <v-img class="align-end text-white"
        src="https://www.acessa.com/_midias/jpg/2022/11/18/400x267/1_parque_da_lajinha-119831.jpg" >
        Parque da Lajinha
      </v-img>
      <v-card-text>
           <div>Lorem Ipsum is simply dummy text of thea </div>
      </v-card-text>
      <v-card-action>
        <v-btn variant="outlined" color="primary">
          Ver Fotos!
        </v-btn>

      </v-card-action>
      </v-card>
      </v-col>



      <v-col cols="12" md="4" lg="3">
      <v-card>

        <v-img class="align-end text-white"
        src="https://midias.correiobraziliense.com.br/_midias/jpg/2022/09/07/675x450/1_o_museu_mariano_procopio_reune_acervo_dos_periodos_colonial_imperial_e_republicano_1_108637-26386222.jpg?20220907102520?20220907102520" >
        Museu Mariano Procópio
      </v-img>

      <v-card-text>
           <div>Lorem Ipsum is simply dummy text of the </div>
      </v-card-text>
      <v-card-action>
        <v-btn variant="outlined" color="primary">
          Ver Fotos!
        </v-btn>
      </v-card-action>
      </v-card>
      </v-col>



      <v-col cols="12" md="4" lg="3">
      <v-card>
        <v-img class="align-end text-white"
        src="https://tribunademinas.com.br/wp-content/uploads/2017/10/c%C3%A2mara.jpg" >
        Parque Halfeld
      </v-img>

      <v-card-text>
           <div>Lorem Ipsum is simply dummy text of the </div>
      </v-card-text>
      <v-card-action>
        <v-btn variant="outlined" color="primary">
          Ver Fotos!
        </v-btn>
      </v-card-action>
      </v-card>
      </v-col>



      <v-col cols="12" md="4" lg="3">
      <v-card>
        <v-img class="align-end text-white"
        src="data:image/jpeg;base64,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" >
        Jardim Botânico da UFJF
      </v-img>

      <v-card-text>
           <div>Lorem Ipsum is simply dummy text of the </div>
      </v-card-text>
      <v-card-action>
        <v-btn variant="outlined" color="primary">
          Ver Fotos!
        </v-btn>
      </v-card-action>
      </v-card>
      </v-col>

   </v-row>
  </v-container>

  <HelloWorld/>
  </v-main>
</v-app>
</template>

<script setup>
import {ref} from "vue";

const isDrawerOpen = ref (false)
</script>
