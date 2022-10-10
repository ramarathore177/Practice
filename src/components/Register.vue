<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="5">
        <v-form ref="form" v-model="valid">
          <v-text-field v-model="name" label="Name" required></v-text-field>
          <v-text-field v-model="email" label="E-mail" required></v-text-field>
          <v-text-field
            v-model="password"
            label="Set Password"
            required
          ></v-text-field>
          <v-text-field
            v-model="password"
            label="Confirm Password"
            required
          ></v-text-field>

          <v-btn color="error" class="mr-4" @click="reset"> Reset Form </v-btn>

          <v-btn color="primary"> Submit </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {};
</script>
