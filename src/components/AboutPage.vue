<template>
    <div id="about-us" class="container">
        <div class="random-box">
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
            <div class="box"></div>
        </div>
        <h1>About Us</h1>

        <div class="content-wrapper">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate quis est magni distinctio
                dignissimos quae modi perferendis nam ad sapiente itaque, provident hic quia vel ut ipsum aliquid rerum
                ea. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio tempora, repellendus aliquid unde
                natus perspiciatis magni impedit corrupti delectus quaerat odit ut? Facere, dolore ipsum eum excepturi
                iure repellat velit.</p>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate quis est magni distinctio
                dignissimos quae modi perferendis nam ad sapiente itaque, provident hic quia vel ut ipsum aliquid rerum
                ea. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio tempora, repellendus aliquid unde
                natus perspiciatis magni impedit corrupti delectus quaerat odit ut? Facere, dolore ipsum eum excepturi
                iure repellat velit.</p>
        </div>
    </div>
</template>

<script>

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap');

.container {
    box-sizing: border-box;

    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 5rem;
    min-height: 100vh;

    padding: 4rem 6rem;
}

@keyframes grow-shrink {
    from {
        transform: scale(1);
    }

    to {
        transform: scale(1.2);
    }
}

.box {
    position: absolute;


    width: 300px;
    height: 300px;
    /* background: rgb(163, 163, 163); */
    background: linear-gradient(to bottom right, rgb(185, 185, 185), rgb(72, 72, 72));
    border-radius: 5px;
    z-index: -1;

    animation-name: grow-shrink;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
    animation-timing-function: ease;
}

.random-box .box:nth-child(1) {
    top: 50%;
    left: 15%;

    animation-delay: 1s;
}

.random-box .box:nth-child(2) {
    top: 5rem;
    left: 5%;

    width: 150px;
    height: 150px;


    animation-delay: 2s;
}

.random-box .box:nth-child(3) {
    top: 28%;
    right: 30%;

    width: 100px;
    height: 100px;


    animation-delay: 5s;
}

.random-box .box:nth-child(4) {
    bottom: 0;
    right: 20%;

    width: 100px;
    height: 100px;

    z-index: 1;

    animation-delay: 3s;
}

.random-box .box:nth-child(5) {
    bottom: 50%;
    right: 5%;

    width: 50px;
    height: 50px;

    z-index: 1;


    animation-delay: 1s;
}


h1 {
    position: relative;
    color: white;
    font-size: 6rem;
    overflow: hidden;
}

h1::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: white;
    width: 100%;
    height: 10px;

    z-index: -1;
    transform: translateX(-101%);
    transition: all 0.2s ease;
}

h1:hover::before {
    transform: translateX(0);
}

.content-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1rem;

    width: 50%;
    min-width: 40rem;
    height: 30rem;
    padding: 4rem;

    background-color: rgba(255, 255, 255, 0.322);
    border: 1px solid white;
    backdrop-filter: blur(1rem);
    border-radius: 1rem;
}

p {
    color: white;
    font-size: 1.5rem;

    font-family: 'Courier New', Courier, monospace;
}
</style>