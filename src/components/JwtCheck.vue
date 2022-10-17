<template>
  <h1>Check Jwt Auth</h1>
  <button @click="getprofile">getprofile</button
  ><button @click="logout">Logout</button>
</template>

<script>
import axios from "axios";
export default {
  name: "JwtCheck",
  methods: {
    async getprofile() {
      let result = await axios
        .get("http://127.0.0.1:8000/api/profile", {
          headers: {
            Authorization: `bearer ${localStorage.getItem("user-token")}`,
          },
        })
        .then((response) => {
          console.log(response);
        })
        .catch((error) => {
          console.log(error);
        });
    },
    logout() {
      localStorage.clear();
    },
  },
};
</script>

<style></style>
