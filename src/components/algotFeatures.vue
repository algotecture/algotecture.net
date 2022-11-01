<template>
  <v-container grid-list-lg>
    <v-layout row>
        <v-flex xs12 class="text-xs-center display-1 font-weight-black my-5 color green lighten-5">Features</v-flex>
    </v-layout>
    <v-layout row wrap>
      <v-flex xs12 sm6 md6>
        <v-card>
          <v-card-title primary-title>
            <div>
                <h3 class="headline mb-0 font-weight-bold">Data control</h3>
                <div style="word-break: break-word" class="spacing-playground pa-3">
                  Upload data to under own sevoerg oenwership
                </div>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm6 md6>
        <v-card>
          <v-card-title primary-title>
            <div>
                <h3 class="headline mb-0 font-weight-bold">Customer layouts</h3>
                <div style="word-break: break-word" class="spacing-playground pa-3">
                  dfd
                </div>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
        <v-layout row wrap>
      <v-flex xs12 sm6 md6>
        <v-card>
          <v-card-title primary-title>
            <div>
                <h3 class="headline mb-0 font-weight-bold">Supporting AI</h3>
                <div style="word-break: break-word" class="spacing-playground pa-3">
                  Coming soon
                </div>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm6 md6>
        <v-card>
          <v-card-title primary-title>
            <div>
                <h3 class="headline mb-0 font-weight-bold">DML</h3>
                <div style="word-break: break-word" class="spacing-playground pa-3">
                  Decentralised Machine Learning (DML) allow AI agents to collaborate Peer to Peer.
                </div>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'CALE-learn',
  data: () => ({
    model: 0
  }),
  methods: {
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
