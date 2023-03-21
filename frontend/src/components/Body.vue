<template>
    <div>
        <b-card id="hydration-level">
            <!-- <div class="aqua-translate">
                                <div class="aqua-flow"></div>
                            </div> -->
            <div class="text-center">
                <div class="aqua-solid">H2O</div>
                <img alt="maleImg" src="../assets/The_maleFinal.png" width="40%" height="35%" class="human-img">
            </div>

            <div class="text-center">Body Vitals</div>
        </b-card>
        <br>
    </div>
</template>

<script>
export default {
    name: 'Body',
    props: {}
}
</script>

<style scoped>
#hydration-level {
    overflow: hidden;
}

.human-img {
    position: relative;
}

.aqua-solid {
    position: absolute;
    height: 100%;
    width: 34%;
    background-color: rgb(19, 227, 255);
    text-align: center;
    bottom: 10%;
    left: 33%;
    color: white;
    overflow-y: inherit;
    animation: aquaAnim 4s ease-out infinite;
}

@media only screen and (max-width: 500px) {
    .aqua-solid {
        max-width: auto;

    }
}

@keyframes aquaAnim {

    0% {
        height: 11px;
    }

    40% {
        height: 100px;
    }

    80% {
        height: 300px;
    }

    80% {
        height: 400px;
    }

    100% {
        height: 11px;
    }
}
</style>
