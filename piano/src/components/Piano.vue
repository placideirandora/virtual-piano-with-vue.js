<template>
  <div class="wrapper">
    <div class="wrapper__piano">
      <div class="wrapper__key wrapper__key--white" @click="playNote('#C')"></div>
      <div class="wrapper__key wrapper__key--black" @click="playNote('#Db')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#D')"></div>
      <div class="wrapper__key wrapper__key--black" @click="playNote('#E')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#Eb')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#F')"></div>
      <div class="wrapper__key wrapper__key--black" @click="playNote('#Gb')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#G')"></div>
      <div class="wrapper__key wrapper__key--black" @click="playNote('#Ab')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#A')"></div>
      <div class="wrapper__key wrapper__key--black" @click="playNote('#Bb')"></div>
      <div class="wrapper__key wrapper__key--white" @click="playNote('#B')"></div>
    </div>

    <audio id="C" src="../assets/notes/C.mp3"></audio>
    <audio id="Db" src="../assets/notes/Db.mp3"></audio>
    <audio id="D" src="../assets/notes/D.mp3"></audio>
    <audio id="E" src="../assets/notes/E.mp3"></audio>
    <audio id="Eb" src="../assets/notes/Eb.mp3"></audio>
    <audio id="F" src="../assets/notes/F.mp3"></audio>
    <audio id="Gb" src="../assets/notes/Gb.mp3"></audio>
    <audio id="G" src="../assets/notes/G.mp3"></audio>
    <audio id="Ab" src="../assets/notes/Ab.mp3"></audio>
    <audio id="A" src="../assets/notes/A.mp3"></audio>
    <audio id="Bb" src="../assets/notes/Bb.mp3"></audio>
    <audio id="B" src="../assets/notes/B.mp3"></audio>
  </div>
</template>

<script>
export default {
  name: "Piano",
  methods: {
    playNote(note) {
      const noteAudio = document.querySelector(note);

      noteAudio.currentTime = 0;
      noteAudio.play();
    }
  }
};
</script>

<style lang="scss" scoped>
*,
*::before,
*::after {
  box-sizing: border-box;
}

.wrapper {
  background: #41b883;
  margin: 0;
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #e9f0f2;

  &__piano {
    display: flex;
  }

  &__key {
    height: calc(var(--width) * 4);
    width: var(--width);
  }

  &__key--white {
    --width: 100px;
    background: #e9f0f2;
    border: 1px solid #2c3e50;
  }

  &__key--black {
    --width: 60px;
    background: #000;
    margin: 0 calc(var(--width) / -2);
    z-index: 2;
  }
}
</style>