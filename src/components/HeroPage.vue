<template>
    <div class="container">
        <div class="bg-img"></div>
        <h1>Élégant</h1>
        <p>" Qui a de l'aisance, de la grâce dans ses manières, son habillement "</p>
        <a href="#about-us" class="button"><img src="../assets/icons/plus-symbol-button.png" width="50%"></a>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.container {
    position: relative;
    display: flex;
    flex-direction: column;

    justify-content: center;
    align-items: center;
    height: 100vh;
}

.bg-img {
    position: absolute;
    width: 100%;
    height: 100%;
    background-image: url('../assets/images/hero-bg.jpg');
    background-size: cover;
    background-position: 0;
    filter: saturate(0) brightness(0.5) blur(0.2rem);
    z-index: -1;

}

h1 {
    color: white;
    font-size: 15rem;
    transition: all 0.5s ease;
}

h1:hover {
    font-size: 18rem;
}

p {
    opacity: 0;
    margin-top: 2rem;

    color: white;
    font-size: 2rem;
    font-family: 'Courier New', Courier, monospace;

    transition: all 0.5s ease;
}

h1:hover ~ p{
    opacity: 1;
}

@keyframes spin {
    from {
        transform: rotate(0deg);
    }

    to {
        transform: rotate(360deg);
    }
}

.button {
    position: absolute;
    bottom: 3rem;

    width: 4rem;
    height: 4rem;
    background-color: white;
    border-radius: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

    font-weight: bolder;
    font-size: 3rem;

    animation-name: spin;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}


</style>