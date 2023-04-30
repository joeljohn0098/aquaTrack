<template>
    <div id="slider">
        <b-container>
            <span class="closebtn" @click="closeSlider">&times;</span>
            <h1 class="big-text text-center">I AM</h1>
            <b-row>
                <b-col sm="6">
                    <div class="maleCard" @mouseenter="toogleMaleBg()" @mouseleave="toggleBg()">
                        <b-card border-variant="primary" header-bg-variant="primary" text-variant="white" header="Male"
                            class="text-center" style="cursor:pointer" @click="closeSlider">
                            <img src="../assets/male-avt.gif" height="100%" width="100%" />
                        </b-card>
                    </div>
                </b-col>
                <b-col sm="6">
                    <div class="femaleCard" @mouseenter="toogleFemaleBg()" @mouseleave="toggleBg()">
                        <b-card border-variant="danger" header-bg-variant="danger" text-variant="white" header="Female"
                            class="text-center" style="cursor:pointer" @click="closeSlider">
                            <img src="../assets/female-avt.gif" height="100%" width="100%" />
                        </b-card>
                    </div>

                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script >

export default {
    name: 'Intro',
    data() {
        return {
        }
    },
    methods: {
        closeSlider: function () {
            //document.getElementById("slider").style.width = "0";
            $('#slider').fadeOut();
            this.$emit('load-content');
        },
        toogleFemaleBg: function () {
            $('#slider').css("background", "radial-gradient(circle, rgb(245, 76, 169) 0%, rgba(140, 175, 217, 1) 100%)");
            console.log('test');
        },
        toogleMaleBg: function () {
            $('#slider').css("background", "radial-gradient(circle, rgb(28, 223, 223) 0%, rgba(140, 175, 217, 1) 100%)");
            console.log('test');
        },
        toggleBg: function () {
            $('#slider').css("background", "radial-gradient(circle, rgb(156, 201, 201) 0%, rgba(140, 175, 217, 1) 100%)");
        }
    },
    mounted() {
    }
};
</script>

<style scoped>
.big-text {
    font-size: 100px;
}

#slider {
    height: 100%;
    width: 100%;
    position: fixed;
    z-index: 1;
    top: 0;
    right: 0;
    background: radial-gradient(circle, rgb(156, 201, 201) 0%, rgba(140, 175, 217, 1) 100%);
    overflow-x: hidden;
    transition: 0.5s;
    padding-top: 60px;
}

#slider .closebtn {
    position: absolute;
    top: 0;
    right: 25px;
    font-size: 36px;
    margin-left: 50px;
    cursor: pointer;
}

.femaleCard {}

.femaleCard :hover {
    box-shadow: 0 44px 18px 0 rgba(255, 0, 191, 0.2);
    transform: scale(1.01);
}


.maleCard {}

.maleCard :hover {
    box-shadow: 0 44px 18px 0 rgba(0, 66, 121, 0.2);
    transform: scale(1.01);

}
</style>