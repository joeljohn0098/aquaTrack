<template>
    <div id="IndexView">
        <Intro @load-content="loadContent" />
        <div id="content">
            <template>
                <b-navbar toggleable type="dark">
                    <b-navbar-brand href="#">
                        <h2>
                            <b-icon icon="droplet-half" aria-hidden="true"></b-icon> AquaTrack
                        </h2>
                    </b-navbar-brand>
                    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                    <b-collapse id="nav-collapse" is-nav>
                        <b-navbar-nav class="ml-auto">
                            <b-nav-item href="#">Reset</b-nav-item>
                        </b-navbar-nav>
                    </b-collapse>
                </b-navbar>
            </template>
            <Content v-if="gender" :selectedGender="gender" />
            <footer class="text-center fixed-bottom">
                <h5> <b-icon icon="droplet-half" aria-hidden="true"></b-icon> AquaTrack Made With Love</h5>
            </footer>
            <div class="d-none d-lg-none d-xl-block">
                <Lottie class="bgm-wave" :options="defaultOptions" :height="1040" v-on:animCreated="handleAnimation" />
            </div>
        </div>
    </div>
</template>
  
<script>
// @ is an alias to /src
import Content from '@/components/Content.vue'
import Intro from '@/components/Intro.vue'
import * as animationData from '@/assets/animations/water-waves.json';

export default {
    name: 'IndexView',
    components: {
        Content, Intro
    },
    data() {
        return {
            defaultOptions: { animationData },
            gender: '',

        }
    },
    methods: {
        handleAnimation: function (anim) {
            anim.setSpeed(0.2);
        },
        loadContent: function (gender) {
            this.gender = gender;
            $('#content').fadeIn(2000);

        }
    },
    mounted() {
        $('#content').hide();
    }
}
</script>

<style scoped>
footer {
    padding: 25px;
    color: white;
}

nav {
    padding: 10px;

}

.bgm-wave {
    bottom: 0;
    position: absolute;
    z-index: -1;
}
</style>
  