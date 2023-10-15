<template>
  <div>
    <h2 class="text-xl font-bold">#Button</h2>
    <div class="flex gap-4">
      <NatButton :config="{ label: 'White', color: 'white', click: () => testEventNatButton('white') }" />
      <NatButton :config="{ label: 'Red', color: 'red', click: () => testEventNatButton('red') }" />
      <NatButton :config="{ label: 'Blue', color: 'blue', click: () => testEventNatButton('blue')  }" />
      <NatButton :config="{ label: 'Green', color: 'green', click: () => testEventNatButton('green') }" />
      <NatButton :config="{ label: 'Orange', color: 'orange', click: () => testEventNatButton('orange') }" />
      <NatButton :config="{ label: 'Pink', color: 'pink', click: () => testEventNatButton('pink') }" />
      <NatButton :config="{ label: 'Fuchsia', color: 'fuchsia', click: () => testEventNatButton('fuchsia') }" />
    </div>
    <div>
      <textarea id="demoNatButton" class="w-full p-4 shadow focus:border-none mt-8"></textarea>
    </div>
    <div>
      <code class="language-html">
        <NatButton :config="{ label: 'White', color: 'white', click: () => testEventNatButton('white') }" />
      </code>
    </div>
  </div>
</template>

<script>
import NatButton from '../components/Button/NatButton.vue';

export default {
  name: 'IndexPage',
  layout: "main",
  components: {
    NatButton
  },
  methods: {
    testEventNatButton(message) {
      document.getElementById("demoNatButton").append(message + "-");
    }
  }
}
</script>

<style scoped>
textarea#story {
  -moz-appearance:none;
  outline:0px none transparent;
}

textarea:focus, input:focus{
    outline: 0;
}
</style>
