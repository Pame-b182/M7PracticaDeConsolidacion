<template>
  <div>
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Cursos AlfaWeb</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn to="/" icon>
        <v-icon>mdi-home</v-icon>
      </v-btn>

      <v-btn to="/admin" icon>
        <v-icon color="white">mdi-wrench</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
    name: 'navbar-component',
    // props: {},
    data: function(){
        return {}
    },
    // computed: {},
    //methods: {}
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    
</style>