<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="12">
        <v-btn
            class="mx-2"
            dark
            large
            color="purple"
            @click="selectedComponent = 'appQuote'"
        >Quote
        </v-btn>
        <v-btn
            @click="selectedComponent = 'appNew'"
            class="mx-2"
            dark
            large
            color="cyan"
        > New
        </v-btn>
        <v-btn
            @click="selectedComponent = 'appAuthor'"
            class="mx-2"
            dark
            large
            color="teal"
        >Author
        </v-btn>
        <hr class="my-2">
        <keep-alive>
          <component :is="selectedComponent">
            <p>default content</p>
          </component>
        </keep-alive>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import AppQuote from "@/components/Quote";
import New from "@/components/New";
import Author from "@/components/Author";

export default {
  name: "appRoot",
  components: {
    appQuote: AppQuote,
    appNew: New,
    appAuthor: Author
  },
  data: () => {
    return {
      selectedComponent: 'appQuote'
    }
  }
}
</script>

<style scoped>
h2 {
  color: red;
}
</style>
