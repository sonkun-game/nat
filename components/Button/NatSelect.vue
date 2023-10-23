<template>
  <div>
    <button class="btn flex justify-between">
      <span> {{ title }} </span>
      <i class="fa-solid fa-chevron-down"></i>
    </button>
  </div>
</template>

<script>
export default {
  name: 'NatSelect',
  props: {
    title: {
      type: String,
      default: "Lựa chọn"
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

