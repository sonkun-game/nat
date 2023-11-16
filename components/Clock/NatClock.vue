<template>
  <div>
    <div v-if="!isDark" class="clock px-4 py-1" :class="{'border-gray-900 border-2':isBorder}">
      <span class="font-bold text-2xl" :class="getColor(color)">{{ currentTime }}</span>
    </div>
    <div v-if="isDark" class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl" :class="getColor(color)">{{ currentTime }}</span>
    </div>

    <!-- <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl text-green-500">{{ currentTime }}</span>
    </div>
    <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl text-blue-500">{{ currentTime }}</span>
    </div>
    <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl text-purple-500">{{ currentTime }}</span>
    </div>
    <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl text-pink-500">{{ currentTime }}</span>
    </div>
    <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}">
      <span class="font-bold text-2xl text-lime-500">{{ currentTime }}</span>
    </div>
    <div class="clock px-4 py-1 bg-gray-900" :class="{'border-gray-600 border-2':isBorder}" style="width: 100px;">
      <span class="font-bold text-2xl text-sky-500">{{ currentTime }}</span>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "NatClock",
  data() {
    return {
      currentTime: ""
    }
  },
  computed: {

  },
  props: {
    isBorder: {
      type: Boolean,
      default: true
    },
    color: {
      type: Boolean,
      default: "black"
    },
    isDark: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    startTime() {
      setInterval(() => {
        console.log("Start Time");
        const today = new Date();
        let h = today.getHours();
        let m = today.getMinutes();
        let s = today.getSeconds();
        m = this.checkTime(m);
        s = this.checkTime(s);
        this.currentTime = h + ":" + m + ":" + s;
      }, 1000);
    },
    checkTime(i) {
      if (i < 10) { i = "0" + i };  // add zero in front of numbers < 10
      return i;
    },
    getColor() {
      if(this.isDark && this.color==='black') {
        return 'text-white'
      } else if(this.color!=='black') {
        return 'text-' + this.color + '-500';
      }
      return 'text-gray-900';
    }
  },
  mounted() {
    this.startTime();
  }
}
</script>

<style scoped>
.clock {
  font-family: 'digital-clock-font';
  width: 95px;
}
</style>

