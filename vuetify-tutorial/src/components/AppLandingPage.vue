<template>
    <v-timeline
    align-top
    :dense="$vuetify.breakpoint.smAndDown"
    >
        <v-timeline-item
        v-for="(item, i) in items"
        :key="i"
        :color="item.color"
        fill-dot
        >
            <v-card
            :color="item.color"
            >
                <v-card-title class="title"> Why Must Housing Payement?</v-card-title>
                <v-card-text class="white text--primary">
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum enim aliquam deleniti, velit, cumque adipisci fugit laudantium suscipit harum laborum sint vero veritatis ex aspernatur.</p>
                    <v-btn
                    :color="item-color"
                    class="mx-0"
                    outlined
                    > Button
                    </v-btn>
                </v-card-text>

            </v-card>

        </v-timeline-item>
    </v-timeline>
</template>

<script>
export default {
    data:() => ({
        items: [
            {color: 'red lighten-2'},
            {color: 'purple darken-2'},
            {color: 'indigo'}

        ]
    })
}
</script>
