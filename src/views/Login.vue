<template>
    <v-container grid-list-md>
        <v-layout justify-center>
           <!-- <v-flex xs6>  -->
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
</template>
<script>
export default {
    data () {
        return {
            show1: false,
            password: 'Password',
            email: 'email'
        }
    }
}
</script>
<style scoped>
</style>