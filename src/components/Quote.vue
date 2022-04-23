<template>
  <div>
    <div class="title">
      <slot name="title"/>
      <span style="color: #CCC">
        <slot name="subtitle">The Subtitle</slot>
      </span>
    </div>
    <div>
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: "appQuote",
  props: {
    quote: String
  }
}
</script>

<style scoped>
.title {
  font-style: italic;
  color: blue;
}

div {
  text-align: center;
  margin: 3% auto;
  padding: 3%;
  border: 1px solid #ccc;
  box-shadow: 1px 1px 2px black;
}

</style>
