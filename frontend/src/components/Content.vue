<template>
    <div>
        <b-container>
            <b-card>
                <h2 class="text-center">Weather & Hydration</h2>
                <b-row>
                    <b-col sm="5">

                        <Body />
                    </b-col>
                    <b-col sm="7">
                        <Weather :selectedGender="selectedGender" />
                        <br>
                        <b-card>
                            <h3 class="text-center">Note</h3>
                            <ul>
                                <li>
                                    When working in the heat, drink 1 cup
                                    (8 ounces) of water every 15–20 minutes.
                                </li>
                                <li>
                                    This translates to ¾–1 quart (24–32 ounces)
                                    per hour.
                                </li>
                                <li>
                                    Drinking at shorter intervals is more effective
                                    than drinking large amounts infrequently.
                                </li>
                            </ul>
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
import Weather from '@/components/Weather.vue'

export default {
    name: 'Content',
    props: { selectedGender: String },
    components: {
        Body,
        Weather
    }
}
</script>

<style>
/* .aqua-flow {
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

} */
</style>

