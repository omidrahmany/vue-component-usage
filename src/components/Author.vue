<template>
  <div>
    <h3>Author component</h3>
    <p>this is author component</p>
    <v-text-field
        label="Our Alive Text"
        hide-details="auto"
        v-model="myDefaultText"
    ></v-text-field>
  </div>
</template>

<script>
export default {
  name: "appAuthor",
  data: () => {
    return {
      myDefaultText: ''
    }
  },
  destroyed() {
    console.log("destroyed!")
  },
  activated() {
    console.log('activated!')
  },
  deactivated() {
    console.log('deactivated!')
  }
}
</script>

<style scoped>

</style>
