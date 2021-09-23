<template>
    <v-container class="keyboard">
      <v-btn @click="changeKeyboardLayout()">UwU</v-btn>
      <KeyboardRow :row="TopRow" :current-key="currentKey"/>
      <KeyboardRow :row="UpperRow" :current-key="currentKey"/>
      <KeyboardRow :row="LowerRow" :current-key="currentKey"/>
      <KeyboardRow :row="BottomRow" :current-key="currentKey"/>
    </v-container>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import QWERTY_keyboardContent from '../static/QWERTY_keyboardContent.json'
import AZERTY_keyboardContent from '../static/AZERTY_keyboardContent.json'
import KeyboardRow from "../components/KeyboardRow";

export default {
  name: "KeyboardHero",
  components: {KeyboardRow},
  data () {
    return {
      targetableKeys: [..."ABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890"],
      currentKey: '',
      pressedKey: '',
      currentLayout: QWERTY_keyboardContent
    }
  },
  created () {
    this.setRandomKey()
  },
  computed: {
    TopRow () {
      return this.currentLayout.filter(key => key.row === 1).sort((x, y) => x.rowIndex - y.rowIndex)
    },
    UpperRow () {
      return this.currentLayout.filter(key => key.row === 2).sort((x, y) => x.rowIndex - y.rowIndex)
    },
    LowerRow () {
      return this.currentLayout.filter(key => key.row === 3).sort((x, y) => x.rowIndex - y.rowIndex)
    },
    BottomRow () {
      return this.currentLayout.filter(key => key.row === 4).sort((x, y) => x.rowIndex - y.rowIndex)
    }
  },
  mounted () {
    window.addEventListener("keypress", (e) => {
      this.pressedKey = e.key
    })
  },
  beforeUnmount () {
    window.removeEventListener("keypress", (e) => {
      this.pressedKey = e.key
    })
  },
  methods: {
    getRandomNumber (min, max) {
      min = Math.ceil(min)
      max = Math.ceil(max)
      return Math.floor(Math.random() * (max - min + 1)) + min
    },
    setRandomKey () {
      this.currentKey = this.targetableKeys[this.getRandomNumber(0, this.targetableKeys.length - 1)]
    },
    changeKeyboardLayout () {
      if (this.currentLayout === QWERTY_keyboardContent) {
        this.currentLayout = AZERTY_keyboardContent
      } else if (this.currentLayout === AZERTY_keyboardContent) {
        this.currentLayout = QWERTY_keyboardContent
      }
    }
  },
  watch: {
    pressedKey: function () {
      if (this.pressedKey.toUpperCase() === this.currentKey) {
        this.setRandomKey()
      }
    }
  }
}
</script>


<style scoped>
/* GENERIC KEYBOARD STYLINGS */
.keyboard {
  display: flex;
  flex-direction: column;
  align-content: center;
  align-items: center;
}
</style>