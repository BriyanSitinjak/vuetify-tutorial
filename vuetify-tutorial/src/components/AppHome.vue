<template>
  <v-app>
    <v-carousel v-model="model">
      <v-carousel-item v-for="(color, i) in colors" :key="color">
        <v-sheet :color="color" height="100%" tile>
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-3">Slide {{ i + 1 }}</div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <v-card class="mx-auto" max-width="344">
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>
      <v-card-title> Our Best Product </v-card-title>
      <v-card-subtitle>
        Housing Payment dapat membantu anda dalam menyelesaikan kebingungan anda
        dalam merekap biaya rumah anda
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
            omnis quasi alias. Expedita ipsam dolorum iste sed error quod
            corrupti inventore deserunt voluptatum blanditiis, iusto voluptatem,
            debitis eaque ab impedit distinctio beatae omnis nulla vitae facilis
            excepturi accusantium, nesciunt placeat. Eum, optio. Cupiditate
            similique nihil ea! Laudantium culpa, iusto sit dolor quam sed. Amet
            laboriosam laudantium quas totam omnis, hic molestias cum eveniet
            aut dolorem veritatis alias minima, tenetur, dolores magnam?
            Deserunt. Similique quam iusto, fuga pariatur quod voluptate, quia
            asperiores esse impedit, labore eius soluta dolorum eum cum in illo
            possimus non architecto quaerat fugiat. Assumenda voluptatum
            incidunt nemo eligendi corrupti. Neque mollitia quaerat maiores ut,
            laboriosam tempore, vitae quo numquam est odit similique, et
            incidunt? Saepe labore voluptas sit eveniet porro! Aspernatur quasi
            provident id libero explicabo, facilis quia consequuntur! Magnam,
            magni. Nostrum obcaecati commodi sunt deleniti iste eligendi
            distinctio ipsa eum nemo, deserunt doloremque vel impedit nisi ad
            ratione ducimus alias debitis quis dolore in, amet totam assumenda
            odio? Dignissimos distinctio sequi quia maiores neque harum debitis
            nesciunt, deserunt dolorum, aliquid omnis totam et, vel reiciendis.
            Nisi, doloremque iure, quisquam magnam iste assumenda corporis
            dolorum, reprehenderit odit rerum rem! Fuga, aperiam earum repellat
            culpa fugit reiciendis vitae velit possimus nihil nostrum, voluptas
            corporis, quasi similique numquam? Labore facilis commodi non.
            Beatae mollitia doloribus aliquam, iure explicabo quisquam sapiente
            tempora! Nisi perferendis veritatis, labore nam iste eum nulla
            voluptates non quia itaque! Esse ipsum voluptas modi distinctio
            eligendi adipisci quod, ducimus in itaque aperiam nemo corrupti
            provident minus mollitia cum! Ratione corporis non, veniam suscipit
            sapiente fugiat, harum possimus voluptas recusandae quos veritatis
            nisi est error debitis iste omnis distinctio assumenda quibusdam ex
            qui corrupti inventore. Quidem ex aliquid consequatur! Ab ipsum
            totam itaque consequuntur natus in eligendi quod, aliquam quae
            voluptatem, laboriosam optio ratione et sit vero molestiae aperiam
            dignissimos nam velit eaque cupiditate nemo hic? Eum, obcaecati id?
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    colors: ["primary", "indigo", "yellow darken-2", "brown", "orange"],
    show: false,
  }),
};
</script>