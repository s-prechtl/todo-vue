<script>

export default {
  name: "todoService",

  data() {
    return {
      headers: '',
      address: '',
      todoURL: '/index.php/?option='
    }
  },
  methods: {
    init() {
      this.headers = {"Content-Type": "application/json"};
      this.address = 'http://localhost:80';
      this.todoURL = '/index.php/?option='
    },

    buildURL(options) {
      return this.address + this.todoURL + options;
    },

    async getTodos() {
      return ((await fetch(this.buildURL("getTodos"))).json())
    }
  }
}
</script>