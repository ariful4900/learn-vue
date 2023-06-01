<script>
export default {
  data() {
    return {
      count: 0,
      name: '',
      names: []
    }
  },
  methods: {
    increment() {
      this.count++
    },
    decrement() {
      if (this.count > 0) {
        this.count--
      }
    },
    addName(e) {
      this.name = e.target.value
    },
    showName() {
      this.names.push(this.name)
      console.log(this.names)
    }
  },
  mounted() {
    this.increment()
  }
}
</script>
<template>
  <div class="count">
    <h1>This is an Counter page</h1>
    <h2>Count is :{{ count }}</h2>
    <div class="btn-group">
      <button @click="decrement">-</button>
      <button @click="increment">+</button>
    </div>
    <div class="input-name">
      <input @change="addName" type="text" /><button @click="showName">Add Name</button>
    </div>
    <div></div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .count {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
}
</style>
