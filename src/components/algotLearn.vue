<template>
  <v-container grid-list-lg>
    <v-layout row>
        <v-flex xs12 class="text-xs-center display-1 font-weight-black my-5 color red accent-2 white--text">Space coherence for the built world</v-flex>
    </v-layout>
    <v-layout row center>
        <v-spacer />
        <v-flex xs12 sm12 md3 class="open-left">
          <v-img src="../assets/logo.png" max-width="400" class="left-perspective">
          </v-img>
          <v-card>
            <v-card-title primary-title>
              <div>
                  <h3 class="headline mb-0 font-weight-bold text-wrap">AgloTecture Toolkit</h3>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>
        <v-flex xs11 sm11 md8 class="open-right">
          <v-carousel class="right-perspective">
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="item.src"
              reverse-transition="fade-transition"
              transition="fade-transition"
            >
              <v-row justify="center" class="middle-top">
                <!-- <v-btn
                  color="orange"
                  x-large
                  elevation="12"
                  raised
                  @click="bboxMobile(item)"
                >
                  {{ item.button.toolkit }}
                </v-btn> -->
                <v-btn
                  color="orange"
                  x-large
                  elevation="12"
                  raised
                  @click="bboxJoin(item)"
                >
                  {{ item.button.mobile }}
                </v-btn>
              </v-row>
            </v-carousel-item>
          </v-carousel>
        </v-flex>
        <v-spacer />
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Algot-learn',
  data: () => ({
    model: 0,
    items: [
      {
        src: require('@/assets/space-coherence.png'),
        button: { mobile: 'Download Toolkit', toolkit: 'Toolkit', bbox: 'climatemodel' }
      }
    ]
  }),
  methods: {
    bboxMobile (select) {
    },
    bboxJoin (select) {
    }
  }
}
</script>

<style scoped>
.open-left {
  margin-top: 3em;
  perspective: 1000px;
}

.left-perspective {
  transform: rotateY(14deg);
}

.open-right {
  perspective: 1000px;
  filter: drop-shadow(10px 20px 55px #B2DFDB);
}

.right-perspective {
  transform: rotateY(-14deg);
}

.middle-top {
  margin-top: 200px;
}
</style>
