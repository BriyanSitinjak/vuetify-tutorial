<template>
  <v-row class="fill-height">
    <v-col cols="12" md="4" class="primary accent-3">
      <v-card-text class="white--text accent-3 mt-14">
        <h1 class="text-center display-1">Welcome Back, Ges</h1>
        <h3 class="text-center mt-4">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </h3>
      </v-card-text>
      <div class="text-center mt-2">
        <v-btn class="white primary--text" rounded outlined @click="step--"
          >SIGN IN</v-btn
        >
      </div>
    </v-col>
    <v-col cols="12" md="8">
      <v-card-text class="mt-12">
        <h1 class="text-center display-2 primary--text text-accent-3">
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
        <h4 class="text-center mt-4">Ensure your email for registration</h4>
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
</template>

<script>
export default {};
</script>