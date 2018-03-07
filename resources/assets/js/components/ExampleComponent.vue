<template>
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            
              <!-- <v-toolbar dark color="indigo"> -->
                <!-- <v-toolbar-title class="white--text"> -->
                  <v-tabs
                    centered
                    color="cyan"
                    dark
                    slider-color="yellow"
                  >
                    <v-tab
                      ripple
                      centered
                    >Login
                    </v-tab>
                    <v-tab
                      ripple
                      centered
                    >New User
                    </v-tab>
                    <v-tab-item>
                      <v-card class="elevation-12">
                        <v-card-text>
                          <v-form>
                            <v-text-field prepend-icon="person" type="text"
                            label="Email"
                            v-model="email"
                            :rules="emailRules"
                            required
                            ></v-text-field>
                            <v-text-field prepend-icon="lock" label="Password" id="password" type="password" 
                            v-model="password"
                            :rules="passwordRules"
                            required></v-text-field>
                          </v-form>
                        </v-card-text>
                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn color="indigo" class="white--text">Login</v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-tab-item>
                    <v-tab-item>
                      <v-card class="elevation-12">
                        <v-card-text>
                          <v-form>
                            <v-text-field prepend-icon="person" type="text"
                            label="Email"
                            v-model="email"
                            :rules="emailRules"
                            required
                            ></v-text-field>
                            <v-text-field prepend-icon="lock" label="Password" id="password" type="password" 
                            v-model="password"
                            :rules="passwordRules"
                            required></v-text-field>
                            <v-text-field prepend-icon="account_circle" label="First Name" id="firstname" type="text" 
                            v-model="firstname"
                            :rules="firstnameRules"
                            required></v-text-field>
                            <v-text-field prepend-icon="account_circle" label="Last Name" id="lastname" type="text" 
                            ></v-text-field>
                            <v-text-field prepend-icon="phone" label="Mobile Number" id="mnumber" type="number" 
                            ></v-text-field>
                          </v-form>
                        </v-card-text>
                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn color="indigo" class="white--text">Register Now</v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-tab-item>
              </v-tabs>
                <!-- </v-toolbar-title> -->
                <!-- <v-spacer></v-spacer> -->
              <!-- </v-toolbar> -->
              
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 20 || 'Name must be less than 20 characters'
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      ],
      password: '',
      passwordRules: [
         v => !!v || 'Password is required',
      ],
      firstname: '',
      firstnameRules: [
         v => !!v || 'Password is required',
      ],
    })
  }
</script>