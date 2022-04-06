<script>

export default {
  name: "todoDetails",

  data() {
    return {
      headers: {"Content-Type": "application/json"},
      address: 'http://localhost:80',
      todoURL: '/index.php/?option='
    }
  },
  methods: {
    buildURL(options) {
      return this.address + this.todoURL + options
    },

    async getTodos() {
      // let options = "getTodos"
      return ((await fetch('http://localhost:80/index.php/?option=getTodos')).json())
    }
  }
}
</script>