<template>
  <p>{{json}}</p>
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
    console.log("bin do")
    this.json = todoService.methods.getTodos()
  }
}
</script>

<style scoped>

</style>