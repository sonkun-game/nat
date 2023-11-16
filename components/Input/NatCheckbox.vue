<template>
  <div>
    <!-- mode 1 -->
    <div  
      v-if="mode === '1'"
      @click="switchCheckbox()" name="container" class="w-16 h-8 cursor-pointer border border-gray-400 rounded-full shadow" :class="{'bg-green-500': isSelect, 'bg-red-500': !isSelect}">
      <div name="bell" :id="bell" class="bell w-8 h-8 bg-white rounded-full border border-gray-400 relative"></div>
    </div>
    <!-- mode 2 -->
    <div  
      v-else-if="mode === '2'"
      @click="switchCheckbox()" name="container" class="w-16 h-8 cursor-pointer border border-gray-400 rounded-full shadow" :class="{'bg-yellow-300': isSelect, 'bg-purple-700': !isSelect}">
      <div name="bell" :id="bell" class="bell w-8 h-8 bg-white rounded-full border border-gray-400 relative"></div>
    </div>
    <!-- mode 3 -->
    <div  
      v-else-if="mode === '3'"
      @click="switchCheckbox()" name="container" class="w-16 h-8 cursor-pointer border border-gray-400 rounded-full shadow" 
      :class="{'bg-night': isSelect, 'bg-dawn': !isSelect}">
      <div name="bell" :id="bell" class="bell w-8 h-8 bg-white rounded-full relative" :class="{'cover-night': isSelect, 'bg-amber-400 border border-amber-400': !isSelect}"></div>
    </div>
    <div v-else>
      <span class="text-red-500">Component NatCheckbox error !</span>
    </div>
  </div>
</template>

<script>
import { v4 as uuidv4 } from 'uuid';

export default {
  name: "NatCheckbox",
  props: {
    isSelect : false,
    mode: {
      type: String,
      default: "1"
    }
  },
  mounted() {
    this.natKey = uuidv4();
    this.bell = 'bell' + this.natKey;
  },
  data() {
    return {
      natKey: "",
      bell: "",
      container: ""
    }
  },
  methods: {
    switchCheckbox() {
      console.log("line 29");
      var btn = document.getElementById(`${this.bell}`);
      if(this.isSelect) {
        btn.style.left = "-1px";
      } else {
        btn.style.left = "32px";
      }
      this.isSelect = !this.isSelect;
      this.$emit('checkbox-change', this.isSelect);
    }
  }
}
</script>

<style scoped>
.bg-night {
  background-image: url('../../assets/img/checkbox/night.jpg');
}
.bg-dawn {
  background-image: url('../../assets/img/checkbox/dawn.jpg');
}
.cover-night {
  background-image: url('../../assets/img/checkbox/moon.jpg');
}
.cover-dawn {
  background-image: url('../../assets/img/checkbox/sun.jpg');
}
.bell {
  top: -1px;
  left: -1px;
  transition: 0.5s;
}
</style>
