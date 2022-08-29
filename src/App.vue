<template>
  <v-app>
    <v-app-bar
      app
      color="primary" 
      dark
    >
      <div class="d-flex align-center">
        <v-text class="display-1">
          Login pages
        </v-text>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href=""
        text
      >
        <span class="mr-2">SignUp</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main class="d-flex align-center">
      <v-row justify="center">
    <v-col
      cols="12"
      sm="8"
      md="6"
      lg="3"
    >

    <v-card>
      <v-form>
    <v-container>

      <h3 class="d-flex justify-center">Login</h3>
      
          <v-text-field
            label="User name"
            placeholder="Eg: nithin123"
            v-model="username"
          ></v-text-field>
           
          <v-text-field
            label="password"
            placeholder="password"
            type="password"
            v-model="password"
          ></v-text-field>
          <i class="fas" :class="{ 'fa-eye-slash': true, 'fa-eye': false }"></i>
          <i class="fas" :class="fa-eye"></i>
        
       
         <v-container class="d-flex justify-center">
           <v-btn
            color="primary"
            text
            @click="submit"
          >
            Submit
          </v-btn>
         </v-container>
      

      </v-container>
      </v-form>

    </v-card>
    </v-col>
    
    </v-row>
    <div v-if="showSubmitValue" class="alignToCenter">
      <v-row><v-text >USERNAME :</v-text>
    <v-text >{{username}}</v-text></v-row>
    <v-row><v-text >PASSWORD :</v-text>
    <v-text >{{password}}</v-text></v-row>
    </div>

    </v-main>
    
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    username: "",
    password: "",
    showSubmitValue: false
  }),
  methods:{
    submit(){
      this.showSubmitValue = true
    }
  }
};
</script>

<style>
.alignToCenter{
  margin-top: 10px;
  margin-left: 590px;
}
</style>