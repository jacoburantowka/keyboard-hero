<template>
    <v-container class="keyboard">
      <ul class="row row-0">
        <li class="pinky" id="esc">ESC</li>
        <li class="pinky" id="1">1</li>
        <li class="ring" id="2">2</li>
        <li class="middle" id="3">3</li>
        <li class="pointer" id="4">4</li>
        <li class="pointer" id="5">5</li>
        <li class="pointer" id="6">6</li>
        <li class="pointer" id="7">7</li>
        <li class="middle" id="8">8</li>
        <li class="ring" id="9">9</li>
        <li class="pinky" id="0">0</li>
        <li class="pinky">-</li>
        <li class="pinky">+</li>
        <li class="pinky" id="back">BACK</li>
      </ul>
      <ul class="row row-1">
        <li class="pinky" id="tab">TAB</li>
        <li class="pinky" id="Q">Q</li>
        <li class="ring" id="W">W</li>
        <li class="middle" id="E">E</li>
        <li class="pointer" id="R">R</li>
        <li class="pointer" id="T">T</li>
        <li class="pointer" id="Y">Y</li>
        <li class="pointer" id="U">U</li>
        <li class="middle" id="I">I</li>
        <li class="ring" id="O">O</li>
        <li class="pinky" id="P">P</li>
        <li class="pinky">[</li>
        <li class="pinky">]</li>
        <li class="pinky">\</li>
      </ul>
      <ul class="row row-2">
        <li class="pinky" id="caps">CAPS</li>
        <li class="pinky" id="A">A</li>
        <li class="ring" id="S">S</li>
        <li class="middle" id="D">D</li>
        <li class="pointer" id="F">F</li>
        <li class="pointer" id="G">G</li>
        <li class="pointer" id="H">H</li>
        <li class="pointer" id="J">J</li>
        <li class="middle" id="K">K</li>
        <li class="ring" id="L">L</li>
        <li class="pinky">:</li>
        <li class="pinky">@</li>
        <li class="pinky" id="enter">ENTER</li>
      </ul>
      <ul class="row row-3">
        <li class="pinky" id="left-shit">SHIFT</li>
        <li class="pinky" id="Z">Z</li>
        <li class="ring" id="X">X</li>
        <li class="middle" id="C">C</li>
        <li class="pointer" id="V">V</li>
        <li class="pointer" id="B">B</li>
        <li class="pointer" id="N">N</li>
        <li class="pointer" id="M">M</li>
        <li class="middle">,</li>
        <li class="ring">.</li>
        <li class="pinky">/</li>
        <li class="pinky" id="right-shift">SHIFT</li>
      </ul>
    </v-container>
</template>

<script>
export default {
  name: "KeyboardHero"
}
</script>

<style scoped>
.keyboard {
  display: flex;
  flex-direction: column;
  align-content: center;
  align-items: center;
}
</style>