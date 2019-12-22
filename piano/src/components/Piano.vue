<template>
    <div class="wrapper">
        <div class="wrapper__piano">
            <div data-note="C" class="wrapper__key wrapper__key--white"></div>
            <div data-note="Db" class="wrapper__key wrapper__key--black"></div>
            <div data-note="D" class="wrapper__key wrapper__key--white"></div>
            <div data-note="E" class="wrapper__key wrapper__key--black"></div>
            <div data-note="Eb" class="wrapper__key wrapper__key--white"></div>
            <div data-note="F" class="wrapper__key wrapper__key--white"></div>
            <div data-note="Gb" class="wrapper__key wrapper__key--black"></div>
            <div data-note="G" class="wrapper__key wrapper__key--white"></div>
            <div data-note="Ab" class="wrapper__key wrapper__key--black"></div>
            <div data-note="A" class="wrapper__key wrapper__key--white"></div>
            <div data-note="Bb" class="wrapper__key wrapper__key--black"></div>
            <div data-note="B" class="wrapper__key wrapper__key--white"></div>
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
    name: 'Piano'
}
</script>

<style lang="scss" scoped>
    *, *::before, *::after {
        box-sizing: border-box;
    }

    .wrapper {
        background: #41B883;
        margin: 0;
        min-height: 50vh;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #E9F0F2;

        &__piano {
            display: flex; 
        }

        &__key {
            height: calc(var(--width) * 4);
            width: var(--width);
        }

        &__key--white {
            --width: 100px;
            background: #E9F0F2;
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