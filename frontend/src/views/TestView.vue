<template>
    <div class="test">
        <div class="content">
        </div>
    </div>
</template>

<script>

</script>

<style scoped>
.content {
    position: relative;
    height: 200px;
    width: 200px;
    background-color: rgb(19, 227, 255);
    align-items: center;
    top: 300px;
    left: 500px;
    animation: animate 4s ease-in-out infinite;
}

@keyframes animate {

    0%,
    100% {
        clip-path: polygon(0% 40%, 18% 36%, 36% 39%, 51% 48%, 69% 61%, 88% 57%, 100% 46%, 100% 100%, 0% 100%);
    }

    50% {
        clip-path: polygon(2% 53%, 19% 67%, 40% 70%, 62% 63%, 77% 51%, 86% 42%, 100% 33%, 100% 100%, 0% 100%);
    }

}
</style>