<template>
  <div class="d-flex justify-center align-center"
    style="height: 100vh">
  <v-card width="400" class="text-center" elevation="12">
  <!--LOGO-->
  <v-icon size="80"  color="red" class="mt-10">mdi-apple</v-icon>
    <v-card-text class="py-10">
       <!--USERNAME TEXT FIELD-->
      <v-text-field variant="outlined" 
      v-model="username"
      flat
      label="username"  
      prepend-inner-icon="mdi-account" 
      clearable
      ></v-text-field>
      <!--PASSWORD TEXT FIELD-->
 <v-text-field variant="outlined" 
      v-model="password"
      flat
      label="password"  
      prepend-inner-icon="mdi-lock" 
      type="password"
      clearable
      ></v-text-field>
       <!--SIGN IN BUTTON-->
      <v-btn color="black" @click="login()" block>Sign in</v-btn>
    </v-card-text>
  </v-card>
  </div>
</template>
<script setup>
definePageMeta({
  layout: "auth",
});
const defaultUsername = ref("admin");
const defaultPassword =  ref("admin123")
const username = ref("");
const password = ref("");
//regular function
function login() {
  alert("Login function called");
}

</script>