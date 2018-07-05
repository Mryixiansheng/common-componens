<template>
    <div>
      <input type="text" v-model="value">
      <key-board  @submit-event='handleSubmit' @change-event='handleChange'></key-board>
    </div>
</template>

<script type="text/ecmascript-6">
/* eslint-disable */
import keyBoard from '../components/keyboard.vue'
export default {
  data () {
    return {
      value: ''
    }
  },
  methods: {
    handleChange(value, currentValue) {
      console.log(value, currentValue);
      this.value = value;
    },
    handleSubmit() {
      console.log('submit: ' + this.value);
    }
  },
  components: {
    keyBoard
  }
}
</script>

<style lang="css" scoped>

</style>
