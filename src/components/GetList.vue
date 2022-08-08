<template>
  <div>
    <form @submit.prevent="createPost">
      <div>
        <label for="userId">login </label>
        <input type="text" id="login" v-model="formData.login" />
      </div>
      <div>
        <label for="userId">email </label>
        <input type="email" id="email" v-model="formData.email" />
      </div>
      <div>
        <label for="userId">password </label>
        <input type="password" id="password" v-model="formData.password" />
      </div>
      <button>Create Post</button>
    </form>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "CreatePost",
  data() {
    return {
      formData: {
        login: "",
        email: "",
        password: "",
      },
    };
  },
  methods: {
    createPost() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.formData)
        .then((response) => console.log(response))
        .catch((error) => console.log(error));
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
