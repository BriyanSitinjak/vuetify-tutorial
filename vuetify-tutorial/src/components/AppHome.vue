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

    <v-container>
      <v-row class="d-flex justify-space-around mb-6">
        <!-- ctrl + shift + i -->
        <v-col v-for="item in data" :key="item" md="4" sm="12" xs="12">
          <v-card v-ripple>
            <v-col>
              <center>
                <v-icon>{{ item.icon }}</v-icon>
                <div v-text="item.title"></div>
                <div v-text="item.desc"></div>
              </center>
            </v-col>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

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

    <!-- add icon on https://pictogrammers.github.io/@mdi/font/2.0.46/ -->
    <!-- <div class="text-center" style="margin: 100px 20px">
      <p class="text-md-h4 font-weight-bold">Why Housing Payment?</p>
      <p class="text-md-subtitle-1">6 Reasons To Use Our Application</p>
      <v-container>
        <v-row>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-icon size="70px" color="primary">mdi-google-maps</v-icon>
              <h2>Deliver to your location</h2>
              <p>Easy Delivery and pick-up from/to your preferred location.</p>
            </v-card>
          </v-col>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-icon size="70px" color="primary">mdi-cellphone-android</v-icon>
              <h2>Easy Booking</h2>
              <p>Select and book your favorite vehicle in just a few clicks.</p>
            </v-card>
          </v-col>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-icon size="70px" color="primary">mdi-shopping</v-icon>
              <h2>Trusted Vendors</h2>
              <p>
                Housing Payment only works with reliable partners and companies.
              </p>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-icon size="70px" color="primary">mdi-google-maps</v-icon>
              <h2>Deliver to your location</h2>
              <p>Easy Delivery and pick-up from/to your preferred location.</p>
            </v-card>
          </v-col>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-badge
                content="Coming Soon"
                color="primary"
                offset-y="-50"
                offset-x="-125"
              ></v-badge>
              <v-icon size="70px" color="primary">mdi-cellphone-android</v-icon>
              <h2>Easy Booking</h2>
              <p>Select and book your favorite vehicle in just a few clicks.</p>
            </v-card>
          </v-col>
          <v-col xs="12" sm="12" md="4">
            <v-card style="padding: 45px 20px">
              <v-icon size="70px" color="primary">mdi-shopping</v-icon>
              <h2>Trusted Vendors</h2>
              <p>
                Housing Payment only works with reliable partners and companies.
              </p>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div> -->

    <div class="text-center" style="margin: 100px 20px 10px 20px">
      <v-rating
        v-model="rating"
        hover
        icon-label="custom icon label text {0} of {1}"
      >
      </v-rating>
    </div>
  </v-app>
</template>

<script>
// import HomeItem from "../data/HomeItem.js";

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
      data: [
        {
          id: 1,
          title: "loremipsumdollor amet 1",
          desc: "loremipsumdollor amet",
          icon: "mdi-account",
        },
        {
          id: 2,
          title: "loremipsumdollor amet 2",
          desc: "loremipsumdollor amet",
          icon: "mdi-account",
        },
        {
          id: 3,
          title: "loremipsumdollor amet 3",
          desc: "loremipsumdollor amet",
          icon: "mdi-account",
        },
      ],
      rating: 4,
    };
  },
};
</script>