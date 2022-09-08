<template>
    <div>
        <h1>Drum Machine</h1>

        <div class="sampleContainer">
            <div class="row">
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
            <div class="row">
                <button v-on:click='playHiHatOpen'>
                    Hi Hat Open
                </button>
                <button v-on:click='playRide'>
                    Ride
                </button>
                <button v-on:click='playCrash'>
                    Crash
                </button>
            </div>
            <div class="row">
                <button v-on:click='playChina'>
                    China
                </button>
                <button v-on:click='playTom1'>
                    Tom 1
                </button>
                <button v-on:click='playTom2'>
                    Tom 2
                </button>
            </div>
        </div>
    </div>
</template>

<script>

const bass = require('../assets/Bass.mp3');
const snare = require('../assets/Snare.mp3');
const hiHatClosed = require('../assets/Hi Hat Closed.mp3');
const hiHatOpen = require('../assets/Hi Hat Open.mp3');
const ride = require('../assets/Ride.mp3');
const crash = require('../assets/Crash.mp3');
const china = require('../assets/China.mp3');
const tom1 = require('../assets/Tom 1.mp3');
const tom2 = require('../assets/Tom 2.mp3');

export default {
    name: 'Machine',
    data: () => ({
        bass,
        snare,
        hiHatClosed,
        hiHatOpen,
        ride,
        crash,
        china,
        tom1,
        tom2
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
        },

        playHiHatOpen: function () {
            let hiHatOpen = new Audio(this.hiHatOpen);
            hiHatOpen.addEventListener("canplaythrough", () => {
                hiHatOpen.play();
            });
        },

        playRide: function () {
            let ride = new Audio(this.ride);
            ride.addEventListener("canplaythrough", () => {
                ride.play();
            });
        },

        playCrash: function () {
            let crash = new Audio(this.crash);
            crash.addEventListener("canplaythrough", () => {
                crash.play();
            });
        },

        playChina: function () {
            let china = new Audio(this.china);
            china.addEventListener("canplaythrough", () => {
                china.play();
            });
        },

        playTom1: function () {
            let tom1 = new Audio(this.tom1);
            tom1.addEventListener("canplaythrough", () => {
                tom1.play();
            });
        },

         playTom2: function () {
            let tom2 = new Audio(this.tom2);
            tom2.addEventListener("canplaythrough", () => {
                tom2.play();
            });
        },
    }
}

</script>

<style>
@import './machine.css';
</style>