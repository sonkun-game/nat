<template>
  <div>
    <button @click="config.click()" class="btn" :class="btnClass">{{ config.label }}</button>
  </div>
</template>

<script>

export default {
  name: 'NatButton',
  data() {
    return {}
  },
  computed: {
    btnClass() {
      switch (this.config.color) {
        case 'white':
          return 'btn bg-white shadow'
        case 'red':
          return 'btn bg-red-600 hover:bg-red-500 text-white shadow'
        case 'blue':
          return 'btn bg-blue-600 hover:bg-blue-500 text-white shadow'
        case 'green':
          return 'btn bg-green-600 hover:bg-green-500 text-white shadow'
        case 'orange':
          return 'btn bg-orange-600 hover:bg-orange-500 text-white shadow'
        case 'pink':
          return 'btn bg-pink-600 hover:bg-pink-500 text-white shadow'
        case 'fuchsia':
          return 'btn bg-fuchsia-600 hover:bg-fuchsia-500 text-white shadow'
      }
      return "btn";
    }
  },
  props: {
    config: {
      label: "Click me",
      color: "white",
      click() {},
    }
  }
}
</script>

<style scoped>
.btn {
  min-width: 150px;
  height: 50px;
  border-radius: 15px;
}
</style>
