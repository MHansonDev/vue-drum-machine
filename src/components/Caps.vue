<template>
    <div class="hello">
        <h1>57 Caps</h1>
        <button v-on:click='playNote'>Play</button>
    </div>
</template>

<script>

const aSound = require('../assets/57 Caps.mp3');

export default {
    name: 'Caps',
    data: () => ({
        aSound,
    }),
    methods: {
        // Selects a note 
        getNote: function () {
            return this.aSound;
        },

        // Plays a note, selected via getNote()
        playNote: function () {
            let note = new Audio(this.aSound);

            note.addEventListener("canplaythrough", () => {
                /* the audio is now playable; play it if permissions allow */
                note.play(); // the audio now can be played
            });
        }
    }
}

</script>