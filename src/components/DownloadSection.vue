<template>
  <section id="download">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img src="@/assets/img/musica.png" class="d-block ml-auto mr-auto" max-width="350px" />
            </v-col>
            <v-col cols="12" sm="8" class="white--text text-left">
              <h1 class="font-weight-light display-2 mb-2">Nueva Cancion</h1>
              <h1 class="font-weight-light">
                Escucha nuestro primer demo "aqui pondria el nombre, si tan solo tuvieramos uno".
              </h1>
              <div>
                <v-btn
                  rounded
                  outlined
                  large
                  color="white"
                  class="mt-4"
                  @click="playAudio"
                >
                  Escuchar/pausar
                </v-btn>

                <audio ref="audioElement" style="display: none">
                  <source :src="audioFile" type="audio/mpeg">
                </audio>

                <div>
                  <v-btn rounded outlined large color="white" class="mt-4" @click="seek(-10)" >
                    Retroceder
                  </v-btn>
                  <v-btn rounded outlined large color="white" class="mt-4" @click="seek(10)" >
                    Adelantar
                  </v-btn>
                  <input type="range" min="0" max="1" step="0.1" v-model="volume" @input="setVolume" />
                </div>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#download {
  background-image: url("~@/assets/img/551126.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
}

#download .container,
#download .row {
  height: 100%;
}
</style>

<script>
export default {
  data() {
    return {
      audioFile: require('@/assets/musica/Owaridemo.mp3'), // Asegúrate de ajustar la ruta a tu archivo MP3
      volume: 1, // Valor inicial del volumen (1 es el volumen máximo)
    };
  },
  methods: {
    playAudio() {
      const audioElement = this.$refs.audioElement;

      if (audioElement.paused) {
        audioElement.style.display = 'block';
        audioElement.play();
      } else {
        audioElement.style.display = 'none';
        audioElement.pause();
      }
    },
    seek(seconds) {
      const audioElement = this.$refs.audioElement;
      audioElement.currentTime += seconds;
    },
    setVolume() {
      const audioElement = this.$refs.audioElement;
      audioElement.volume = this.volume;
    },
  },
};
</script>
