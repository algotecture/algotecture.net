<template>
  <v-container grid-list-lg>
    <v-row no-gutters center>
      <v-spacer />
      <v-col
        cols="7"
      >
        <v-flex class="ai-converse">
          <v-card
            class="pa-6"
            outlined
            color="transparent"
          >
            Peer----- {{ question }}
          </v-card>
          <v-card
            class="pa-4"
            outlined
            color="transparent"
          >
            {{ cale }} -- CALE
          </v-card>
        </v-flex>
        <v-form
            ref="form"
            v-model="valid"
            lazy-validation
            class="conversation-form"
          >
            <v-text-field
              v-model="question"
              :counter="50"
              :rules="nameRules"
              label="question"
              required
            ></v-text-field>

            <!-- <v-text-field
              v-model="email"
              :rules="emailRules"
              label="E-mail"
              required
            ></v-text-field> -->

            <!-- <v-select
              v-model="select"
              :items="items"
              :rules="[v => !!v || 'Item is required']"
              label="Item"
              required
            ></v-select> -->

            <!-- <v-checkbox
              v-model="checkbox"
              :rules="[v => !!v || 'You must agree to continue!']"
              label="Do you agree?"
              required
            ></v-checkbox> -->

            <v-btn
              :disabled="!valid"
              color="success"
              class="mr-4"
              @click="validate"
            >
              Ask Aglotecture
            </v-btn>

            <v-btn
              color="error"
              class="mr-4"
              @click="reset"
            >
              clear input
            </v-btn>

            <!-- <v-btn
              color="warning"
              @click="resetValidation"
            >
              Reset Validation
            </v-btn> -->
          </v-form>
          <download-toolkit v-if="downloadStateTK === true"></download-toolkit>
      </v-col>
      <v-spacer />
    </v-row>
  </v-container>
</template>

<script>
import DownloadToolkit from '@/components/download/downloadToolkit'

export default {
  name: 'cale-ai',
  components: {
    DownloadToolkit
  },
  data: () => ({
    valid: true,
    question: '',
    cale: '',
    downloadStateTK: false,
    nameRules: [
      v => !!v || 'A question is required',
      v => (v && v.length < 51) || 'only short question'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid'
    ],
    select: null,
    items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4'
    ],
    checkbox: false
  }),
  methods: {
    validate () {
      const passV = this.$refs.form.validate()
      console.log(passV)
      if (passV === true) {
        this.askCale()
      }
    },
    askCale () {
      // send message to peerlink to Cale
      if (this.question === 'hello') {
        this.cale = 'how can CALE help?'
      } else if (this.question === 'mobile') {
        this.cale = 'CALE mobile app can help, please download or use webapp <btn>DOWNLOAD APP</btn>,'
      } else {
        this.cale = 'Sorry CALE has no data to help answer that. Download a BentoBox Toolkit to add it to the network <btn>DOWNLOAD</btn>,'
        this.downloadStateTK = true
      }
    },
    reset () {
      this.$refs.form.reset()
      this.downloadStateTK = false
    },
    resetValidation () {
      this.$refs.form.resetValidation()
    }
  }
}
</script>

<style scoped>
.conversation-form {
  border: 2px solid red;
}

.ai-converse {
  border: 2px solid blue;
  margin-bottom: 1em;
}
</style>
