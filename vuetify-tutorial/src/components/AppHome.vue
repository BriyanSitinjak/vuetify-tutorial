<template>
  <v-app>
    <v-carousel height="90vh">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>

    <!-- <v-card class="mx-auto" max-width="344">
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>
      <v-card-title> Our Best Product </v-card-title>
      <v-card-subtitle>
        Housing Payment dapat membantu anda dalam menyelesaikan kebingungan anda
        dalam merekap biaya rumah
      </v-card-subtitle>
      <v-card-actions>
        <v-btn color="grey darken-2"> Explore </v-btn>

        <v-spacer></v-spacer>

        <v-btn icon @click="show = !show">
          <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>
          <v-card-text>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel
            consequatur est quia nam aliquam doloremque assumenda impedit magni
            quibusdam accusamus error perspiciatis hic odit sunt, quisquam
            possimus reprehenderit obcaecati? Mollitia? Perspiciatis minima
            sapiente harum libero et fugit officiis illum natus omnis odio quo
            sequi, minus, quis nostrum consequatur dolorem commodi assumenda
            dolore incidunt illo ab! Consectetur necessitatibus quis aliquam
            commodi. Magnam quibusdam dicta, velit commodi eius minima neque
            ratione voluptates. Vel minima illum corrupti velit placeat, aperiam
            tenetur totam eos sunt labore fugiat nobis voluptates culpa ipsa a
            aliquid? Quo? Obcaecati officiis aut vitae distinctio sint. Ea
            exercitationem assumenda hic quo laudantium dolor numquam
            consectetur ipsa, vitae dolorum nisi voluptatum officiis quas
            veritatis voluptates quam nemo tenetur id culpa cupiditate! Rerum
            ipsa vitae maiores sapiente in libero est omnis nesciunt nemo
            laborum voluptas aliquid placeat debitis, dolores assumenda ad
            voluptatibus doloremque impedit quaerat dolor. Expedita officia vel
            omnis quasi alias.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card> -->

    <div class="text-center" style="margin:100px 20px;">
      <p class="text-md-h4 font-weight-bold">Why Housing Payment?</p>
      <p class="text-md-subtitle-1"> 6 Reasons To Use Our Application</p>
      <v-container>
      <v-row>
        <v-col xs="6">
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
        <v-col xs="6">
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
        <v-col xs="6">
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row>
        <v-col>
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
        <v-col>
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
        <v-col>
          <v-card>
            <h2>Briyan Sitinjak</h2>
            <p>Clansitinjak</p>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    </div>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
        },
      ],
    };
  },
};
</script>