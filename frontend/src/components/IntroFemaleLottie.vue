<template>
    <div class="IntroFemaleLottie">
        <Lottie :options="defaultOptions" :height="600" v-on:animCreated="" />
    </div>
</template>

<script >
import * as animationData from '@/assets/animations/fAvatar.json';

export default {
    name: 'IntroFemaleLottie',
    components: {
    },
    data() {
        return {
            defaultOptions: { animationData },

        }
    },
    methods: {
        handleAnimation: function (anim) {
            anim.setSpeed(0.2);
        },
    }
}
</script>

<style scoped></style>