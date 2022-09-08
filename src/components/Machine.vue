<template>
    <div>
        <h1>Drum Machine</h1>

        <div class="row1">
            <button v-on:click='playBass'>
                Bass
            </button>
            <button v-on:click='playSnare'>
                Snare
            </button>
            <button v-on:click='playHiHatClosed'>
                Hi Hat closed
            </button>
        </div>
    </div>
</template>

<script>

const bass = require('../assets/Bass.mp3');
const snare = require('../assets/Snare.mp3');
const hiHatClosed = require('../assets/Hi Hat Closed.mp3');

export default {
    name: 'Machine',
    data: () => ({
        bass,
        snare,
        hiHatClosed
    }),
    methods: {
        playBass: function () {
            let bass = new Audio(this.bass);
            bass.addEventListener("canplaythrough", () => {
                bass.play();
            });
        },

        playSnare: function () {
            let snare = new Audio(this.snare);
            snare.addEventListener("canplaythrough", () => {
                snare.play();
            });
        },

        playHiHatClosed: function () {
            let hiHatClosed = new Audio(this.hiHatClosed);
            hiHatClosed.addEventListener("canplaythrough", () => {
                hiHatClosed.play();
            });
        }
    }
}

</script>

<style>
@import './machine.css';
</style>