<template>
<div>
   <!-- <v-container grid-list-md>
        <v-layout justify-center>
               <v-flex xs6>
                <v-card>
                <v-form @submit.prevent="onSubmit">
                    <div class="input :class="{invalid: $v.email.$error}">"
                    <v-text-field 
                    label="Email"
                    @blur="$v.email.$touch()"
                    placeholder="your_email@gmail.com"
                    v-model.lazy="email">
                    </v-text-field>
                    <p v-if="!$v.email.email">Please provide a valid email address.</p>
                    </div>

                    <v-text-field
                    class="input"
                    label="Error"
                    v-model="password"
                    :type="show1 ? 'text' : 'password'">
                    :rules="[rules.required.Min]"
                    validate-on-blur
                    error
                    value="PA"
                    >  
                    </v-text-field>
                    <p v-if="!$v.password.required">Please provide a password.</p>
                    <p v-if="">Please provide at least</p>
                </v-form>
                </v-card>
            </v-flex>
            <div>
                <p>{{ email }}</p>
                <p> {{ password }} </p>
                </div>
        </v-layout>
    </v-container>
-->
   
 <v-layout row justify-center>
    <v-dialog v-model="dialog" persistent max-width="600px">
      <v-btn slot="activator" color="primary" dark>Login</v-btn>
      <v-card>
        <v-card-title>
          <span class="headline">User Login</span>
        </v-card-title>
        <v-card-text>
          <v-container grid-list-md>
            <v-layout wrap>
              
              <v-flex xs12>
                <v-text-field label="Email*" required></v-text-field>
              </v-flex>
              <v-flex xs12>
                <v-text-field label="Password*" type="password" required></v-text-field>
              </v-flex>
              
            </v-layout>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" flat @click.native="dialog = false">Close</v-btn>
          <v-btn color="blue darken-1" flat @click.native="dialog = false">Submit</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-layout>

</div>
</template>
<script>
/*
 export default {
    data () {
        return {
            show1: false,
            password: '',
            email: 'email',
            rules: {
            required: value => !!value || 'Password is Required.',
            min: v => v.length >= 8 || 'Min 8 characters',
    },
        }
    },
    validations: {
        email: {
            required,
            email
        },
    },

    methods: {
        onSubmit() {
            console.log('Thanks for submitting!')
        }
    }
}
*/

 export default {
    data: () => ({
      dialog: false
    })
  }
  
</script>
<style scoped>

</style>