<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="5">
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-text-field
            v-model="name"
            :rules="nameRules"
            label="Name"
            required
          ></v-text-field>

          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>

          <!-- <v-checkbox
                v-model="checkbox"
                :rules="[v => !!v || 'You must agree to continue!']"
                label="Do you agree?"
                required
                ></v-checkbox> -->

          <v-btn color="success" class="mr-4" @click="submit"> Validate </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>
