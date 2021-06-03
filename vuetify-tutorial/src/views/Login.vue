<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 primary--text text--accent-3"
                        >
                          Sign In Now
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-google</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          Ensure your email for registration
                        </h4>
                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="primary accent-3"
                          />
                          <v-text-field
                            id="password"
                            label="Password"
                            name="Password"
                            prepend-icon="lock"
                            type="password"
                            color="primary accent-3"
                          />
                        </v-form>
                        <h5 class="text-center mt-3">Forget Your Passsword?</h5>
                      </v-card-text>
                      <div class="text-center mb-3">
                        <v-btn rounded color="primary accent-3">
                          SIGN IN
                        </v-btn>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="primary accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1 mt-2">Hello, Ges</h1>
                        <h3 class="text-center mt-4">
                          Lorem ipsum dolor sit amet consectetur adipisicing
                        </h3>
                      </v-card-text>
                      <div class="text-center mt-2">
                        <v-btn
                          rounded
                          outlined
                          class="white primary--text"
                          @click="step++"
                          >SIGN UP</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="primary accent-3">
                      <v-card-text class="white--text accent-3 mt-14">
                        <h1 class="text-center display-1">Welcome Back, Ges</h1>
                        <h3 class="text-center mt-4">
                          Lorem ipsum dolor sit amet consectetur adipisicing
                          elit.
                        </h3>
                      </v-card-text>
                      <div class="text-center mt-2">
                        <v-btn
                          class="white primary--text"
                          rounded
                          outlined
                          @click="step--"
                          >SIGN IN</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 primary--text text-accent-3"
                        >
                          Create Account
                        </h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon> fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-google</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">
                          Ensure your email for registration
                        </h4>
                        <v-form>
                          <v-text-field
                            color="primary accent-3"
                            label="Name"
                            name="Name"
                            prepend-icon="person"
                            type="text"
                          ></v-text-field>
                          <v-text-field
                            color="primary accent-3"
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                          ></v-text-field>
                          <v-text-field
                            color="primary accent-3"
                            label="Password"
                            name="Password"
                            prepend-icon="lock"
                            type="password"
                          ></v-text-field>
                        </v-form>
                      </v-card-text>
                      <div class="text-center mb-4">
                        <v-btn color="primary accent-3" rounded>SIGN UP</v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    step: 1,
  }),
};
</script>














































<!-- <template>
  <v-container>
    <form>
      <v-text-field
        v-model="name"
        :error-messages="nameErrors"
        :counter="10"
        label="Full Name"
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
      ></v-text-field>
      <v-text-field
        v-model="email"
        :errormessage="emailErrors"
        label="Email"
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
      ></v-text-field>
      <v-select
        v-model="select"
        :items="items"
        :error-messages="selectErrors"
        label="Item"
        required
        @change="$v.select.$touch()"
        @blur="$v.select.$touch()"
      ></v-select>
      <v-checkbox
        v-model="checkbox"
        :error-messages="checkboxErrors"
        label="Saya Bersedia Mendaftar"
        required
        @change="$v.checkbox.$touch()"
        @blur="$v.checkbox.$touch()"
      ></v-checkbox>

      <v-btn class="mr-4" @click="submit"> MASUK </v-btn>

      <v-btn @click="clear"> HAPUS DATA </v-btn>
    </form>
  </v-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],

  validations: {
    name: { required, maxLength: maxLength(10) },
    email: { required, email },
    select: { required },
    checkbox: {
      checked(val) {
        return val;
      },
    },
  },

  data: () => ({
    name: "",
    email: "",
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
  }),

  computed: {
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked &&
        errors.push("Kamu harus menyetujui untuk melanjutkannya!");
      return errors;
    },
    selectErrors() {
      const errors = [];
      if (!this.$v.select.$dirty) return errors;
      !this.$v.select.required && errors.push("Pilih salah satu item!");
      return errors;
    },
    nameErrors() {
      const errors = [];
      if (!this.$v.name.dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Nama Lengkap minimal 10 karakter!");
      !this.$v.name.required && errors.push("Lengkapi nama anda!");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email &&
        errors.push("Harus menggunakan email yang valid!");
      !this.$v.email.required && errors.push("Lengkapi Email anda!");
      return errors;
    },
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.select = null;
      this.checkbox = false;
    },
  },
};
</script> -->