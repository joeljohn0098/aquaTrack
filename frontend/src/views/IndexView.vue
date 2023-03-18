<template>
    <div id="content">
        <b-navbar toggleable="lg" type="dark" variant="primary" class="fixed-top">
            <b-navbar-brand href="#">
                AquaTrack
            </b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item href="#">Link</b-nav-item>
                    <b-nav-item href="#">Link2</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>


        <Content />
        <footer class="text-center bg-primary">
            <p> AquaTrack Made With Love</p>
        </footer>
    </div>
</template>
  
<script>
// @ is an alias to /src
import Content from '@/components/Content.vue'


export default {
    name: 'IndexView',
    components: {
        Content
    }
}
</script>

<style scoped>
footer {
    padding: 25px;
    color: white;
}

#content {
    background-color: rgb(157, 216, 255);
}

nav {
    padding: 10px;
}
</style>
  