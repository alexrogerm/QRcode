<template>
  <div class="gradient-input">
    <div>
      <input type="color" v-model="hexCode" @input="handleInput('input-value2', hexCode)">
      <input type="text" v-model="hexCode" @input="handleInput('input-value2', hexCode)">
    </div>
    <div>
      <input type="color" v-model="hexCode2" @input="handleInput('input-value3', hexCode2)">
      <input type="text" v-model="hexCode2" @input="handleInput('input-value3', hexCode2)">
    </div>
    <div>
      <label>MaskPattern:</label>
      <input type="number" v-model.number="MaskPattern" min="0"
        @input="handleMPInput('input-value4', MaskPattern)" /><span>px</span>
    </div>
    <div>
      <label>Scale: </label>
      <input type="number" v-model.number="Scale" min="0"
        @input="handleScaleInput('input-value5', Scale)" /><span>px</span>
    </div>
  </div>
</template>
<script>
export default {
  name: "ContentTwo",
  emits: ['input-value2', 'input-value3', 'input-value4', 'input-value5'],
  data() {
    return {
      hexCode: '#000000',
      hexCode2: '#ffffff',
      MaskPattern: 0,
      Scale: 4,
    }
  },
  methods: {
    handleInput(emitEvent, value) {
      this.$emit(emitEvent, value)
    },
    handleMPInput(emitEvent, value) {
      this.$emit(emitEvent, value)
    },
    handleScaleInput(emitEvent, value) {
      this.$emit(emitEvent, value)
    }
  }
}
</script>