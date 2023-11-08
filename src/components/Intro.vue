<template>
    <div class="intro" id="intro">
        <Header class="intro_header"></Header>
        <h1 class="intro__title">Assalamu Aleykum</h1>
        <p class="intro__subtitle"> <span></span> Explore Our World <span></span></p>

        <div class="intro__main ">
            <div class="intro__main__left">
                <div class="intro__main__left__item">
                    <div class="intro__main__left__item-info">
                        <h1>We meet deadlines</h1>
                        <p>Your deadline is the most important value for us. Our job is to make sure the job is done perfectly before the deadline.</p>
                    </div>
                    <div class="intro__main__left__item__icon">
                        <div class="rectangular">
                        </div>
                        <i class="fa fa-calendar"></i>
                    </div>
                </div>

                <div class="intro__main__left__item">
                    <div class="intro__main__left__item-info">
                        <h1>Communication is key</h1>
                        <p>Our team is available to check on your questions and take in feedback as soon as possibly.</p>
                    </div>
                    <div class="intro__main__left__item__icon">
                        <div class="rectangular">
                        </div>
                        <i class="fa fa-comments"></i>
                    </div>
                </div>
            </div>
            <div class="intro__main__center">
                <div class="intro__main__center__rectangular"></div>
            </div>

            <div class="intro__main__right">
                <div class="intro__main__right__item">

                    <div class="intro__main__right__item__icon">
                        <div class="rectangular">

                        </div>
                        <i class="fa fa-check"></i>
                    </div>
                    

                    <div class="intro__main__right__item-info">
                        <h1>Quality Control</h1>
                        <p>We test out everything to make sure that your project is fully functional, cross–browser compatible and meets your specifications.</p>
                    </div>
                    
                </div>

                <div class="intro__main__right__item">

                    <div class="intro__main__right__item__icon">
                        <div class="rectangular">

                        </div>
                        <i class="fa fa-list"></i>
                    </div>

                    <div class="intro__main__right__item-info">
                        <h1>PIXEL PERFECT</h1>
                        <p>We develop meaningful digital products and experiences that matter with design thinking and creative craftsmanship.</p>
                    </div>
                   
                </div>
            </div>

            
        </div>
    </div>
</template>

<script>
    import Header from "./Header.vue";  
    export default {
        
        components: {
            Header,
        }

    }
</script>

<style>
    .intro_header{
        position: absolute;
        top: 0;
        left: 0;
        z-index: 99;
    }
    .intro{
        background-color: white;
        /* height: 100vh; */
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        flex-direction: column;
        width: 100%;
        padding-top: 100px;
    }

    .intro__title{
        font-size: 32px;
        font-family: 'Varela (woff2)',sans-serif;
        font-weight: 500;
        color: #196FC4;
    }

    .intro__subtitle{
        color: #666666;
        font-size: 16px;
        display: inline-block;
        display: flex;
        align-items: center;
        gap: 20px;
    }

    .intro__subtitle span{
        height: 1.3px;
        width: 15px;
        background-color: #666666;
    }

    .intro__main{
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 30px;
        padding: 0 30px;
        width: 80%;
        margin: 50px auto;
        flex-wrap: wrap;
        row-gap: 60px;
    }
   
    .intro__main__center{
        width: 25%;
    }
   
    .intro__main__center__rectangular{
        position: absolute;
        top: 45%;
        left: 43%;
        margin: 0 auto;
        width: 200px;
        height: 200px;
        background-color: #196FC2;
        transform: rotate(45deg);
    }

    .intro__main__left{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 50px;
        width: 30%;
    }

    .intro__main__right{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 50px;
        width: 30%;
    }

    .intro__main__right__item{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .intro__main__left__item{
        display: flex;
        align-items: center;
        justify-content: space-between;

    }
    
    .intro__main__left__item-info{
        width: 70%;
    }

    .intro__main__right__item-info{
        width: 75%;
    }

    .intro__main__left__item__icon{
        width: 50px;
        height: 50px;

        position: relative; 
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .intro__main__left__item-info h1{
        font-size: 16px;
        font-weight: 700;
        font-family:"Open Sans",sans-serif;
        text-transform: uppercase;
        margin-bottom: 20px;
    }

    .intro__main__right__item-info h1{
        font-size: 16px;
        font-weight: 700;
        font-family:"Open Sans",sans-serif;
        text-transform: uppercase;
        margin-bottom: 20px;
    }

    .intro__main__right__item-info p{
        font-size: 12px;
        font-weight: 300;
        font-family:"Open Sans",sans-serif;
        text-transform: uppercase
    }

    .intro__main__left__item-info p{
        font-size: 12px;
        font-weight: 300;
        font-family:"Open Sans",sans-serif;
        text-transform: uppercase
    }


    .intro__main__right__item__icon{
        width: 50px;
        height: 50px;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .intro__main__left__item__icon i{
        font-size: 24px;
    }

    .intro__main__right__item__icon i{
        font-size: 24px;
    }

    .rectangular{
        position: absolute;
        width: 100%;
        height: 100%;
        box-shadow: 5px 5px 0  rgb(144, 140, 140);
        transform: rotate(45deg);
        border: 1px solid rgb(144, 140, 140);

    }

    @media only screen and (max-width: 900px){
        .intro__main__center{
            display: none;
        }

        .intro__main__right{
            width: 45%;
        }

        .intro__main__left{
            width: 45%;
        }

        .intro__main__left__item__icon{
            width: 40px;
            height: 40px;
        }

        .intro__main__right__item__icon{
            width: 40px;
            height: 40px;
        }

        .intro__main__left__item-info p{
            font-size: 10px;
        }

        .intro__main__right__item-info p{
            font-size: 10px;
        }

        .intro__main__right__item-info h1{
            font-size: 14px;
        }

        .intro__main__left__item-info h1{
            font-size: 14px;
        }
    }

    @media only screen and (max-width: 700px){
        .intro__main__left{
            width: 100%;
        }

        .intro__main__right{
            width: 100%;
        }

        .intro__title{
            font-size: 24px;
        }

        .intro{
            padding-top: 150px;
        }
    }
</style>

