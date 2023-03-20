<template>
    <div>
        <b-card>
            <!-- <div class="aqua-translate">
                                <div class="aqua-flow"></div>
                            </div> -->
            <div class="aqua-solid">H2O</div>
            <div class="text-center human-img">
                <img alt="maleImg" src="../assets/The_maleFinal.png" width="40%" height="35%">
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
.human-img {
    position: relative;
}

.aqua-solid {
    position: absolute;
    height: 100%;
    width: 34%;
    background-color: rgb(19, 227, 255);
    text-align: center;
    bottom: 92px;
    left: 33%;
    color: white;
    animation: aquaAnim 4s ease-out infinite;
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
