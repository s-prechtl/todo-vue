<template>

    <div v-for="object in json" :key="object">
      <h1 @click="listingClicked(object.id)">{{object.name}}</h1>
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
    listingClicked(id){
      console.log(id)
    }
  },
  mounted() {
    todoService.methods.init();
    todoService.methods.getTodos().then(result => {
      this.json = result;
    })
  }
}
</script>

<style scoped>

</style>