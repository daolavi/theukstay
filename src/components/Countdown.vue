<template>
    <div class="block">
        <p class="digit">{{ days }}</p>
        <p class="text">Days</p>
    </div>
    <div class="block">
        <p class="digit">{{ hours }}</p>
        <p class="text">Hours</p>
    </div>
    <div class="block">
        <p class="digit">{{ minutes }}</p>
        <p class="text">Minutes</p>
    </div>
    <div class="block">
        <p class="digit">{{ seconds }}</p>
        <p class="text">Seconds</p>
    </div>
</template>
<script>
export default {

    ready() {
        window.setInterval(() => {
            this.now = Math.trunc((new Date()).getTime() / 1000);
        },1000);
    },

    props : {
        date : {
            type: Number,
            coerce: str => Math.trunc(Date.parse(str) / 1000)
        }
    },

    data() {
        return {
            now: Math.trunc((new Date()).getTime() / 1000)
        }
    },

    computed: {
        seconds() {
            let seconds = (this.date - this.now) % 60
            let seconds_two_digits = seconds.toString().padStart(2,'0')
            return seconds_two_digits
        },

        minutes() {
            let minutes = Math.trunc((this.date - this.now) / 60) % 60
            let minutes_two_digits = minutes.toString().padStart(2,'0')
            return minutes_two_digits
        },

        hours() {
            let hours = Math.trunc((this.date - this.now) / 60 / 60) % 24
            let hours_two_digits = hours.toString().padStart(2,'0')
            return hours_two_digits
        },

        days() {
            let days = Math.trunc((this.date - this.now) / 60 / 60 / 24)
            return days
        }
    }
}

</script>
<style>
@import url(https://fonts.googleapis.com/css?family=Roboto+Condensed:400|Roboto:100);

.block {
    display: flex;
    flex-direction: column;
    margin: 20px;
}

.text {
    color: #acb1f1;
    font-size: 40px;
    font-family: 'Roboto Condensed', serif;
    font-weight: 400;
    margin-top:10px;
    margin-bottom: 10px;
    text-align: center;
}

.digit {
    color: #acb1f1;
    font-size: 150px;
    font-weight: 100;
    font-family: 'Roboto', serif;
    margin: 10px;
    text-align: center;
}
</style>
