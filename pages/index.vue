<template>
  <div>
    <!-- Nat Button Example-->
    <div id="NatButtonID" class="mb-8 border">
      <h2 class="text-xl font-bold">#Button</h2>
      <div class="flex gap-4">
        <NatButton :config="{ label: 'White', color: 'white', click: () => testEventNatButton('white') }" />
        <NatButton :config="{ label: 'Red', color: 'red', click: () => testEventNatButton('red') }" />
        <NatButton :config="{ label: 'Blue', color: 'blue', click: () => testEventNatButton('blue') }" />
        <NatButton :config="{ label: 'Green', color: 'green', click: () => testEventNatButton('green') }" />
        <NatButton :config="{ label: 'Orange', color: 'orange', click: () => testEventNatButton('orange') }" />
        <NatButton :config="{ label: 'Pink', color: 'pink', click: () => testEventNatButton('pink') }" />
        <NatButton :config="{ label: 'Fuchsia', color: 'fuchsia', click: () => testEventNatButton('fuchsia') }" />
      </div>
      <div>
        <textarea id="demoNatButton" class="w-full p-4 shadow focus:border-none mt-8"></textarea>
      </div>
      <div>
        <h3 class="text-lg font-bold">#example</h3>
        <pre>
          <code class="language-markup w-full block">
            <!-- test -->
            &lt;NatButton :config="{ label: 'White', color: 'white', click: () => testEventNatButton('white') }" />
            &lt;NatButton :config="{ label: 'Red', color: 'red', click: () => testEventNatButton('red') }" />
            &lt;NatButton :config="{ label: 'Blue', color: 'blue', click: () => testEventNatButton('blue') }" />
            &lt;NatButton :config="{ label: 'Green', color: 'green', click: () => testEventNatButton('green') }" />
            &lt;NatButton :config="{ label: 'Orange', color: 'orange', click: () => testEventNatButton('orange') }" />
            &lt;NatButton :config="{ label: 'Pink', color: 'pink', click: () => testEventNatButton('pink') }" />
            &lt;NatButton :config="{ label: 'Fuchsia', color: 'fuchsia', click: () => testEventNatButton('fuchsia') }" />
        </code>
      </pre>
      </div>
    </div>

    <!-- Nat Select Example-->
    <div id="NatSelect" class="mb-8 border">
      <h2 class="text-xl font-bold">#NatSelect</h2>
      <div class="flex gap-4">
        <NatSelect></NatSelect>
      </div>
      <div>
        <textarea id="demoNatSelect" class="w-full p-4 shadow focus:border-none mt-8"></textarea>
      </div>
      <div>
        <h3 class="text-lg font-bold">#example</h3>
        <pre>
          <code class="language-markup w-full block">
          </code>
        </pre>
      </div>
    </div>

    <!-- Nat Checkbox Example-->
    <div id="NatCheckbox" class="mb-8 border">
      <h2 class="text-xl font-bold">#NatCheckbox</h2>
      <div class="flex gap-4">
        <NatCheckbox />
        <NatCheckbox mode="2" />
        <NatCheckbox mode="3" />
      </div>
      <div>
        <h3 class="text-lg font-bold">#example</h3>
        <pre>
          <code class="language-markup w-full block">
            &lt;NatCheckbox />
            &lt;NatCheckbox mode="2" />
            &lt;NatCheckbox mode="3" />
          </code>
        </pre>
      </div>
    </div>

        <!-- Nat Clock Example-->
        <div id="NatClock" class="mb-8 border">
      <h2 class="text-xl font-bold">#NatClock</h2>
      <div class="flex gap-4">
        <NatClock :is-dark="false"></NatClock>
        <NatClock :is-dark="false" color="green"></NatClock>
        <NatClock :is-dark="false" color="blue"></NatClock>
        <NatClock :is-dark="false" color="red"></NatClock>
        <NatClock :is-dark="false" color="purple"></NatClock>
        <NatClock :is-dark="true"></NatClock>
        <NatClock :is-dark="true" color="green"></NatClock>
        <NatClock :is-dark="true" color="blue"></NatClock>
        <NatClock :is-dark="true" color="red"></NatClock>
        <NatClock :is-dark="true" color="purple"></NatClock>
      </div>
      <div>
        <h3 class="text-lg font-bold">#example</h3>
        <pre>
          <code class="language-markup w-full block">
            &lt;NatClock :is-dark="false">&lt;/NatClock>
            &lt;NatClock :is-dark="false" color="green">&lt;/NatClock>
            &lt;NatClock :is-dark="false" color="blue">&lt;/NatClock>
            &lt;NatClock :is-dark="false" color="red">&lt;/NatClock>
            &lt;NatClock :is-dark="false" color="purple">&lt;/NatClock>
            &lt;NatClock :is-dark="true">&lt;/NatClock>
            &lt;NatClock :is-dark="true" color="green">&lt;/NatClock>
            &lt;NatClock :is-dark="true" color="blue">&lt;/NatClock>
            &lt;NatClock :is-dark="true" color="red">&lt;/NatClock>
            &lt;NatClock :is-dark="true" color="purple">&lt;/NatClock>
          </code>
        </pre>
      </div>
    </div>
  </div>
</template>

<script>
import NatButton from '../components/Button/NatButton.vue';
import NatSelect from '../components/Button/NatSelect.vue';
import NatCheckbox from '../components/Input/NatCheckbox.vue';
import NatClock from '../components/Clock/NatClock.vue';

export default {
  name: 'IndexPage',
  layout: "main",
  components: {
    NatButton,
    NatSelect,
    NatCheckbox,
    NatClock
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
  -moz-appearance: none;
  outline: 0px none transparent;
}

textarea:focus,
input:focus {
  outline: 0;
}
</style>
