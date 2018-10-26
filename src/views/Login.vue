<template>
   <!-- <v-container grid-list-md>
        <v-layout justify-center>
               <v-flex xs6>
                <v-card>
                <v-form>
                    <v-text-field label="Email"
                    placeholder="foo@bar.com"
                    v-model="email">
                    </v-text-field>

                    <v-text-field
                    label="Password"
                    v-model="password"
                    :type="show1 ? 'text' : 'password'">  
                    </v-text-field>
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


</template>
<script>
/* export default {
    data () {
        return {
            show1: false,
            password: 'Password',
            email: 'email'
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