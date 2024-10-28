<template>
    <div class="image-container">
        <img src="@/assets/cat_inside_color.jpg" alt="Background Image" class="image" style="z-index: 1;">
        <img src="@/assets/coat_outside.png" alt="Top Image" class="image top-image" style="z-index: 2;">
    </div>
</template>

<script>
export default {
    mounted() {
        const topImage = document.querySelector('.top-image');
        topImage.addEventListener('click', () => {
            topImage.classList.toggle('slide');
        });
    }
}
</script>

<style>
body {
    background-color: rgb(24, 24, 24);
    margin: 0;
    padding: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.image-container {
    position: relative;
    width: 200px;
    height: 600px;
}

.image {
    position: absolute;
    width: 200px;
    height: 600px;
    top: 0;
    left: 0;
    transition: transform 0.5s ease;
}

.top-image {
    top:-13%;
    height: 750px;
}

.image.slide {
    transform: translateX(200px);
}
</style>
