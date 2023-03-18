<template>
    <div>
        <br><br><br>
        <b-container>
            <b-card>
                <p class="text-center">
                    Body Vitals
                </p>
                <b-row>
                    <b-col>
                        <b-card>
                            <div class="aqua-translate">
                                <div class="aqua-flow"></div>
                            </div>
                            <div class="aqua-solid"></div>
                            <div class="text-center human-img">
                                <img alt="maleImg" src="../assets/The_maleFinal.png" width="50%" height="50%">
                            </div>

                        </b-card>
                    </b-col>
                    <b-col>
                        <b-card>
                            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been
                            the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley
                            of type and scrambled it to make a type specimen book. It has survived not only five centuries,
                            but also the leap into electronic typesetting, remaining essentially unchanged. It was
                            popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages,
                            and more recently with desktop publishing software like Aldus PageMaker including versions of
                            Lorem Ipsum
                            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been
                            the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley
                            of type and scrambled it to make a type specimen book. It has survived not only five centuries,
                            but also the leap into electronic typesetting, remaining essentially unchanged. It was
                            popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages,
                            and more recently with desktop publishing software like Aldus PageMaker including versions of
                            Lorem Ipsum
                        </b-card>
                    </b-col>
                </b-row>

            </b-card>
        </b-container>
        <br>
    </div>
</template>

<script>
export default {
    name: 'Content',
    props: {}
}
</script>

<style>
.card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    padding: 30px;
}

.card:hover {
    box-shadow: 0 18px 16px 0 rgba(0, 0, 0, 0.2);
}

.human-img {
    position: relative;
}

.aqua-flow {
    position: absolute;
    height: 200px;
    width: 246px;
    background-color: rgb(19, 227, 255);
    align-items: center;
    bottom: 474px;
    left: 170px;
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

.aqua-solid {
    position: absolute;
    height: 370px;
    width: 246px;
    background-color: rgb(19, 227, 255);
    align-items: center;
    bottom: 104px;
    left: 170px;
}

.aqua-translate {
    animation-name: aquaTranslate;
    animation-duration: 4s;
}

@keyframes aquaTranslate {

    0% {
        bottom: 474px;
    }

    25% {
        bottom: 500px;
    }

    50% {
        bottom: 550px;
    }

    75% {
        bottom: 600px;
    }

    100% {
        bottom: 650px;
    }
}
</style>

