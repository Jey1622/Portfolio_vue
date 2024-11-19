<template>
  <v-container class="pa-5">
    <v-row align="center" justify="center">
      <v-col cols="12" md="8">
        <h1 class="headline">Contact Me</h1>
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-text-field
            v-model="name"
            :rules="[v => !!v || 'Name is required']"
            label="Name"
            required
          ></v-text-field>
          <v-text-field
            v-model="email"
            :rules="[v => !!v || 'Email is required', v => /.+@.+\..+/.test(v) || 'E-mail must be valid']"
            label="Email"
            required
          ></v-text-field>
          <v-textarea
            v-model="message"
            :rules="[v => !!v || 'Message is required']"
            label="Message"
            required
          ></v-textarea>
          <v-btn
            :disabled="!valid"
            color="primary"
            @click="submitForm"
          >
            Submit
          </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      valid: false,
      name: '',
      email: '',
      message: ''
    };
  },
  methods: {
    submitForm() {
      if (this.$refs.form.validate()) {
       
        console.log('Form Submitted:', {
          name: this.name,
          email: this.email,
          message: this.message
        });
        
        this.$refs.form.reset();
      }
    }
  }
};
</script>

<style scoped>
.headline {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 25px;
  text-align: center;
}
</style>
