<template>
  <v-row>
    <v-col class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
    <v-col>
      <v-card>
        <v-btn @click="increment()">
          Click to Increment
        </v-btn>
        <v-card-title>
          Counter
        </v-card-title>
        <v-card-text>
          {{ count }}
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import { mapMutations } from 'vuex';

export default {
  name: 'InspirePage',
  computed: {
    count() {
      return this.$store.state.counter
    }
  },
  methods: {
    ...mapMutations({
      increment: 'increment'
    })
  }
}
</script>
