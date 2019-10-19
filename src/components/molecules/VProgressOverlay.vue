<template>
  <v-overlay :value="status">
    <v-progress v-if="status === 'PROGRESS'" size="15vw"></v-progress>
    <v-success v-else-if="status === 'SUCCEED'" size="15vw"></v-success>
    <v-failure v-else-if="status === 'FAIL'" size="15vw"></v-failure>
  </v-overlay>
</template>

<script>
import { mapGetters } from 'vuex'
import VProgress from '~/components/atoms/VProgress'
import VSuccess from '~/components/atoms/VSuccess'
import VFailure from '~/components/atoms/VFailure'
export default {
  components: {
    VProgress,
    VSuccess,
    VFailure
  },

  computed: {
    ...mapGetters('progress', ['status'])
  }
}
</script>

<style></style>
