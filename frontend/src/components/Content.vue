<template>
    <div>
        <b-container>
            <b-card>
                <h2 class="text-center">Water & Hydration</h2>
                <b-row>
                    <b-col sm="5">

                        <Body />
                    </b-col>
                    <b-col sm="7">
                        <b-card>
                            <h3 class="text-center">Current Weather</h3>
                            <div class="text-center">
                                <!-- weather widget start --><a target="_blank"
                                    href="https://www.booked.net/weather/kerala-32462"><img
                                        src="https://w.bookcdn.com/weather/picture/1_32462_1_1_137AE9_160_ffffff_333333_08488D_1_ffffff_333333_0_6.png?scode=40569&domid=w209&anc_id=54881"
                                        alt="booked.net" /></a><!-- weather widget end -->
                            </div>
                        </b-card>
                        <br>
                        <b-card>
                            <h3 class="text-center">Drink 4 glass of water to stay hydrated</h3>
                        </b-card>
                    </b-col>
                </b-row>

            </b-card>
        </b-container>
        <br>
    </div>
</template>

<script>
import Body from '@/components/Body.vue'

export default {
    name: 'Content',
    props: {},
    components: {
        Body
    }
}
</script>

<style>
.aqua-flow {
    position: absolute;
    height: 200px;
    width: 132px;
    background-color: rgb(19, 227, 255);
    bottom: 251px;
    left: 177px;
    animation: animate 4s ease-in-out infinite;
}

@keyframes animate {

    0%,
    100% {
        clip-path: polygon(0 80%, 11% 74%, 24% 67%, 34% 66%, 43% 67%, 53% 74%, 61% 81%, 67% 86%, 76% 91%, 91% 94%, 100% 85%, 100% 100%, 0 100%);
    }

    50% {
        clip-path: polygon(0 83%, 10% 88%, 23% 92%, 34% 95%, 44% 89%, 53% 79%, 63% 69%, 75% 65%, 84% 66%, 94% 68%, 100% 73%, 100% 100%, 0 100%);
    }

}
</style>

