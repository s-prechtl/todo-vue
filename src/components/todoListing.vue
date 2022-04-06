<template>
  <div v-for="object in json">
    {{object}}
  </div>
</template>

<script>
import todoService from "@/components/todoService";

export default {
  name: "todoListing",
  data() {
    return {
      json: ""
    }
  },
  methods: {

  },
  mounted() {
    this.json = JSON.parse(todoService.methods.getTodos())
  }
}
</script>

<style scoped>

</style>