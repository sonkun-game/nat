<template>
  <div class="p-16 flex gap-2">
    <NatClockVue :is-dark="false"></NatClockVue>
    <NatClockVue :is-dark="false" color="green"></NatClockVue>
    <NatClockVue :is-dark="false" color="blue"></NatClockVue>
    <NatClockVue :is-dark="false" color="red"></NatClockVue>
    <NatClockVue :is-dark="false" color="purple"></NatClockVue>
    <NatClockVue :is-dark="true"></NatClockVue>
    <NatClockVue :is-dark="true" color="green"></NatClockVue>
    <NatClockVue :is-dark="true" color="blue"></NatClockVue>
    <NatClockVue :is-dark="true" color="red"></NatClockVue>
    <NatClockVue :is-dark="true" color="purple"></NatClockVue>
  </div>
</template>

<script>
import NatCheckbox from '../../components/Input/NatCheckbox.vue';
import NatClockVue from '../../components/Clock/NatClock.vue';

export default {
  components: {
    NatCheckbox,
    NatClockVue
  }
}
</script>

<style>

</style>

