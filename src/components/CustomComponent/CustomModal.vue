<template>
  <v-dialog :width="width" :value="value">
    <v-card class="px-4 py-4">
      <h3 class="text-body-1">{{ header }}</h3>
      <v-flex class="py-5 d-flex justify-end" padless fixed>
        <v-btn class="mr-2" color="primary" text @click="emit('cancel')">
          {{ cancel }}
        </v-btn>
        <v-btn color="primary" @click="emit('ok')">
          {{ ok }}
        </v-btn>
      </v-flex>
    </v-card>
  </v-dialog>
</template>
<script>
export default {
  name: "custom-modal",
  props: {
    width: {
      type: Number,
      default: 500,
    },
    value: {
      type: Boolean,
      default: false,
    },
    header: {
      type: String,
      default: "Are You Sure ?",
    },
    cancel: {
      type: String,
      default: "Cancel",
    },
    ok: {
      type: String,
      default: "Confirm",
    },
  },
};
</script>
