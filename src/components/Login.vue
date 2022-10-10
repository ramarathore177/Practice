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
          <v-btn color="primary" class="mr-4" @click="showModal=true"> Validate </v-btn>
          <v-btn color="primary" text @click="register"> Register </v-btn>
        </v-form>
      </v-col>
    </v-row>
    <custom-modal :value="showModal">    
    </custom-modal>
  </v-container>
</template>
<script>
import CustomModal from "./CustomComponent/CustomModal.vue"
export default {
  components:{
    CustomModal
  },
 data() {
   return {
       showModal: false
   }
 }
  
}
</script>