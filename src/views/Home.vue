<template>
  <v-container fluid fill-height>
    <div class="algot-waves">
      <algot-learn></algot-learn>
      <!-- <algotecture></algotecture> -->
      <algot-features></algot-features>
      <algot-usecases></algot-usecases>
      <algot-footer></algot-footer>
    </div>
  </v-container>
</template>

<script>
// import Algotecture from '@/components/algotecture'
import AlgotLearn from '@/components/algotLearn'
import AlgotFeatures from '@/components/algotFeatures'
import AlgotUsecases from '@/components/algotUsecases'
import AlgotFooter from '@/components/algotFooter'

export default {
  name: 'Algotecture-Content',
  components: {
    // Algotecture,
    AlgotLearn,
    AlgotFeatures,
    AlgotUsecases,
    AlgotFooter
  }
}
</script>

<style>
.algot-waves {
  background-color: 'green lighten-5';
  background-position: center center;
  background-repeat: repeat-y;
  width: 100%;
  height: 100%;
}
</style>
