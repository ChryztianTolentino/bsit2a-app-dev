<template>
      <div class="d-flex align-center justify-center" 
      style="height: 100vh;">

           <v-card width="400" class="text-center" elevation="12">

                    <!-- logo -->
             <v-icon size="75" color="red" class="pt-10">mdi-apple</v-icon>

                <v-card-text class="py-10">
                
                    <!-- Username textfield-->
                    <v-text-field
                        variant="outlined"
                        v-model="username"
                        label="Username" 
                        prepend-inner-icon="mdi-account"
                        clearable
                    ></v-text-field>

                    <!-- Password -->
                    <v-text-field
                        variant="outlined"
                        v-model="password"
                        label="Password"
                        type="password"
                        prepend-inner-icon="mdi-lock"
                        clearable
                    ></v-text-field>

                    <!-- sign in button  -->
                    <v-btn color="red" @click="login()" block>
                        Sign In
                    </v-btn>

                </v-card-text>
           </v-card>
      </div>
</template>

<script setup>
definePageMeta({
    layout: 'auth',
});

const defaultUsername = ref("Admin")
const defaultPassword = ref("Admin123")
const username = ref("")
const password = ref("")

// login
function login() {
  alert('Galing!!! Nahulaan mo!!!');
}


// arrow
// const loginForm = () => {
// }

</script>