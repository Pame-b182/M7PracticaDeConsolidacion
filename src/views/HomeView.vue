<template>
  <v-container>
    <h1 class="text-center">Lista de Cursos</h1>
    <v-row justify="space-around">
      <v-card v-for="curso in cursos" :key="curso.id" class="mt-8 mx-1" width="290">
        <v-img contain height="200px" :src="curso.img">
          <v-app-bar flat color="rgba(0, 0, 0, 0)"> </v-app-bar>
        </v-img>
        <h4 class="text-center mt-5">{{ curso.nombre }}</h4>
        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">Información</div>

          <v-timeline align-top dense>
            <v-timeline-item small color="deep-purple lighten-1">
              <div>
                <div class="font-weight-normal">
                  Costo: <strong>${{ curso.costo }}</strong>
                </div>
                <div>Duración: {{ curso.duracion }}</div>
              </div>
            </v-timeline-item>
            <v-timeline-item small color="green">
              <div>
                <div class="font-weight-normal">
                  Cupos: <strong>{{ curso.cupos }}</strong>
                </div>
                <div>Completado: {{ cursoTerminado(curso.id) }}</div>
              </div>
            </v-timeline-item>
            <v-timeline-item small color="deep-purple lighten-1">
              <div>
                <div class="font-weight-normal">
                  Fecha de Registro:
                </div>
                <div>{{ curso.fecha_registro }}</div>
              </div>
            </v-timeline-item>
             <v-timeline-item small color="green">
              <div>
                <div class="font-weight-normal">
                  Descripción
                </div>
                <div>{{ curso.descripcion}}</div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>


<script>
import { mapState, mapGetters } from "vuex";
export default {
  name: "home-view",
  // props: {},
  data: function () {
    return {};
  },
  computed: {
    ...mapState(["cursos"]),
    ...mapGetters(["cursoTerminado"]),
  },
  //methods: {}
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
};
</script>

<style scoped>
</style>