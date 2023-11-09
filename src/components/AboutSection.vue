<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2 white--text">Datos sobre los panawaris</h1>
              <br>
              <v-row>
                <h3 class="text-justify white--text">Dato de nuestro debut: </h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/band.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    en nuestro debut no contabamos con un 'encore', siendo por esto repetimos una cancion del setlist a pedido del publico 'tears dont fall'.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">Influencias musicales: </h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/influencias.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    Dentro de nuestras influencias musicales se encuentran bandas como: Trivium, Bullet For My Valentine,
                    Killswitch Engage, Bring Me The Horizon, A Day To Remember, entre otros.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">"Basthy" Vocalista:</h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/basthy.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    Basthy, Basthy Joestar, Bastian José Estrellas, Alaias pa los amigos.
                    <br>
                    Fanboy del mundo manga, anime y videojuegos, sobre todo lo que tenga que ver con Asano Inio y el One Piece es real. 
                    <br>
                    Enamoraoh' de Hollow Knigth, Legend of Zelda y Silent Hill. 
                    <br>
                    Sus bandas favoritas son Radiohead, Ice nine kills, BMTH y ADTR.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">"Wino" Primera Guitarra:</h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/wino.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    guitarrista desde los 12 años, siendo partícipe en dos bandas actualmente. 
                    <br>
                    Es lolero por lo que es repelente al agua, le gusta ver series, videos de música y sacarse riffs complejos pero nunca la canción completa. 
                    <br>
                    Desde muy pequeño se entusiasmó por la música ya que su hermano (el baterista) escuchaba este género, tales bandas como Killswitch Engage, 
                    Trivium, As I Lay Dying son parte de su inspiración al componer riffs para la banda. 
                    <br>
                    Actualmente Wino se encuentra estudiando Tecnología Médica y es feliz siendo parte de Owari.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">"Pipe" Segunda Guitarra:</h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/pipe.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    Guitarrista desde que iba en el colegio, Ing en sonido de profesión, el Pipeckless o Vendaval Estudios, maldito lolero, 
                    fanático de la música en general, sus listas de Spotify van desde el reggaetón más cochino, hasta un deathcore satánico.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">"Loki" Bajo y segunda voz:</h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/loki.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    Loki, elioth, kazu
                    <br>
                    Bajista de los 8 años, cuenta la leyenda que le habia llamado a su bajo "shadow", le apasiona la musica japonesa como toda la cultura de aquel pais,
                    el mas friki de la banda, dicen que no se baña (es otaku).
                    <br>
                    Sus bandas favoritas son Trivium, Simple plan y Kizu.
                  </p>
                </v-col>
                <br>
                <h3 class="text-justify white--text">"Josi" Bateria:</h3>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/Jose.png"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify white--text">
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  </p>
                </v-col>
              </v-row>
              <br>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <div>
                <video ref="videoElement" :src="videoFile" controls style="width: 500px; height:700px;"></video>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      videoFile: require('@/assets/musica/360live.mp4'), // Asegúrate de ajustar la ruta a tu video
    };
  },
  methods: {
    playVideo() {
      this.$refs.videoElement.play();
    },
    pauseVideo() {
      this.$refs.videoElement.pause();
    },
    seekVideo(seconds) {
      this.$refs.videoElement.currentTime += seconds;
    },
  },
};
</script>

<style scoped>
#about {
  background: linear-gradient(to left, #000000, #800000);
}
</style>
