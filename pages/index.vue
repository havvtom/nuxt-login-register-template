<template>
  <v-row align="center" justify="center">
    <v-col cols="12" sm="10">
      <v-card class="elevation-6 mt-10">
        <v-window v-model="step">
          <v-window-item :value="1">
            <v-row>
              <v-col cols="12" sm="6">
                <v-card-text class="mt-12">
                  <h4 class="text-center">Login in to Your Account</h4>
                  <h6 class="text-center grey--text">Login in to your account so you can continue building<br>and editing your onboarding flows</h6>
                  <v-row align="center" justify="center">
                    <v-col cols="12" sm="8">
                      <v-text-field label="Email" outlined dense color="blue" automplete="false" class="mt-16"></v-text-field>
                      <v-text-field label="Password" outlined dense color="blue" automplete="false" type="password"></v-text-field>
                      <v-row>
                        <v-col cols="12" sm="7">
                          <v-checkbox label="Remember Me" class="mt-1" color="blue"></v-checkbox>
                        </v-col>
                        <v-col cols="12" sm="5">
                          <span class="caption blue--text">Forget password</span>
                        </v-col>
                      </v-row>
                      <v-btn color="blue" dark block tile>Login</v-btn>
                    </v-col>
                  </v-row>
                </v-card-text>
              </v-col>
              <v-col cols="12" sm="6" class="blue rounded-bl-xl">
                <div style="txt-align:center; padding:180px 0;">
                  <v-card-text class="white--text">
                    <h3 class="text-center">Don't have an account yet? Register</h3>
                    <h6 class="text-center">
                      Let's get you all set up so you can start creating your first<br>onboarding experience
                    </h6>
                  </v-card-text>
                  <div class="text-center">
                    <v-btn tile outlined dark @click="step++">Sign Up</v-btn>
                  </div>
                </div>
              </v-col>
            </v-row>
          </v-window-item>
          <v-window-item :value="2">
            <v-row>
              <v-col cols="12" sm="6" class="blue rounded-br-xl">
                <div style="text-align:center; padding: 180px 0;">
                  <v-card-text class="white--text">
                    <h3 class="text-center">Already signed up?</h3>
                    <h6>Log into your account so you can continue building and<br>editing your onboarding flows</h6>
                  </v-card-text>
                  <div class="text-center">
                    <v-btn tile outlined dark @click="step--">Login</v-btn>
                  </div>
                </div>
              </v-col>
              <v-col cols="12" sm="6">
                <v-card-text class="mt-12">
                  <h4 class="text-center">Sign up for an Account</h4>
                  <h6 class="text-center grey--text">
                    Let's get you all set up so you can start creating your<br>first onboarding experience
                  </h6>
                  <v-row align="center" justify="center">
                    <v-col cols="12" sm="8">
                      <v-row>
                        <v-col cols="12" sm="6">
                          <v-text-field label="First Name" outlined dense color="blue" autocomplete=""false class="mt-4"></v-text-field>
                        </v-col>
                        <v-col cols="12" sm="6">
                          <v-text-field label="Last Name" outlined dense color="blue" autocomplete=""false class="mt-4"></v-text-field>
                        </v-col>
                      </v-row>
                      <v-text-field label="Email" outlined dense color="blue" autocomplete=""false class="mt-4"></v-text-field>
                      <v-text-field label="Password" outlined dense color="blue" autocomplete=""false class="mt-4"></v-text-field>
                      <v-text-field label="Confirm Password" outlined dense color="blue" autocomplete=""false class="mt-4"></v-text-field>
                      <v-btn color="blue" dark block tile>Sign Up</v-btn>
                    </v-col>
                  </v-row>
                </v-card-text>
              </v-col>
            </v-row>
          </v-window-item>
        </v-window>
      </v-card>
    </v-col>
  </v-row>
</template>
<script type="text/javascript">
  export default{
    data () {
      return {
        step: 1,

      }
    }
  }
</script>
<style>
    .v-application .rounded-bl-xl {
      border-bottom-left-radius: 300px !important;
    }
    .v-application .rounded-br-xl {
      border-bottom-right-radius: 300px !important;
    }
</style>