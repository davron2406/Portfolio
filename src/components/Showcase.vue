<template>
    <div class="showcase" id="home">
        <div class="showcase__main">
            <h1>I am Davron Saydullayev</h1>
            <h2>I'm a creative web developer</h2>
            <h3>I stand on a sweet spot where design & code intersects</h3>
        </div>
    </div>

</template>

<style>
    .showcase{
        background-image: url("../assets/images/photo_2023-09-28_10-09-51.jpg");
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .showcase__main{
        text-transform: uppercase;
        font-family: "Open Sans",sans-serif;
        text-align: center; 
        color: white
    }

    .showcase__main h1{
        font-size: 40px;
        padding: 0 15px;
    }

    .showcase__main h2{
        font-size: 18px;
        padding: 10px 0;
        display: inline-block;
        border-bottom: 2px solid white;

    }

    .showcase__main h3{
        font-size: 14px;
        margin-top: 10px;
    }
</style>