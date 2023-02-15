<template>
  <div id="app">
    <h1>Book show | Hide</h1>
    <div v-if="showBook">
      <p>{{ title }} - {{ author }} - {{ age }}</p>
    </div>
    <button @click="toggleShowBook">
      <span class="btn1" v-if="showBook">Hide Book</span>
      <span class="btn2" v-else>Show Book</span>
    </button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showBook: true,
      title: "O'tkan kunlar",
      author: "Abdulla Qodiriy",
      age: 1969,
    };
  },
  methods: {
    toggleShowBook() {
      this.showBook = !this.showBook;
    },
  },
};
</script>
<style>
button {
  cursor: pointer;
  padding: 0;
  border: none;
}
.btn1,
.btn2 {
  font-size: 18px;
  color: #fff;
  padding: 5px 7px;
}
.btn1 {
  background-color: green;
}

.btn2 {
  background-color: red;
}
</style>

<!-- <template>
  <div>
    <p>Full name: {{ fullName }}</p>
    <p>
      <label for="firstName">First name:</label>
      <input id="firstName" type="text" v-model="firstName" />
    </p>
    <p>
      <label for="lastName">Last name:</label>
      <input id="lastName" type="text" v-model="lastName" />
    </p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
    };
  },
  computed: {
    fullName() {
      return this.firstName + " " + this.lastName;
    },
  },
};
</script>
<style></style> -->
