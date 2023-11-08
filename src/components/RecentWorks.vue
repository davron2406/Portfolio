<template>
    <div class="recent__works" id="works">
        <div class="container70">
            <h1 class="recent__works__title">RECENT WORKS</h1>
            <p class="recent__works__subtitle">OUR CLIENTS LOVE US! READ WHAT THEY HAVE TO SAY</p>
            <div class="recent__works__cards">
                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">WEB SITE</p>
                        <p class="recent__work__group">Web Development</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works2.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">Program for Learning center</p>
                        <p class="recent__work__group">Web Development</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works3.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works4.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works5.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works6.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works3.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

                <div class="recent__works__card">
                    <div class="link">
                        <div class="rectangular">
                            
                        </div>
                        <a href="#"><i class="fa fa-plus"></i></a>
                    </div>
                    <div class="recent__work__img">
                        <img src="../assets/images/recent__works.jpg" alt="">
                    </div>
                    <div class="recent__work__info">
                        <p class="recent__work__name">PSD Template</p>
                        <p class="recent__work__group">Web Design</p>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>


<style>
    .recent__works{
        background: white;
        padding-top: 100px;
        padding-bottom: 100px;
    }

    .recent__works__title{
        text-align: center;
        color: #196fc2;
    }

    .recent__works__subtitle{
        text-align: center;
        color: #666666;
        margin-top: 10px;
        margin-bottom: 30px;
    }

    .recent__works__cards{
        display: flex;
        flex-wrap: wrap;
    }

    .recent__works__card{
        width: 25%;
        position: relative;
        overflow: hidden;
        height: 250px;
    }

    .recent__work__img{
        height: 100%;
        transition: all .5s ease;
        position: relative;
    }

    .recent__work__img::after{
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 0;
        background: #1970c295;
    }

    .recent__work__img img{
        width: 100%;
        height: 100%;
    }

    .recent__work__info{
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        background-color: white;
        width: 100%;
        height: 75px;   
        transition: all .5s ease;
        transform: translateY(75px);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        opacity: 0;
        visibility: hidden;
    }

    .recent__works__card:hover .recent__work__img{
        height: 70%; 
    }

    .recent__works__card:hover .recent__work__img::after{
        height: 100%;
    }

    .recent__works__card:hover .recent__work__info{
        visibility: visible;
        opacity: 1;
        transform: translateY(0);
    }

    .recent__works__card:hover .link{
        visibility: visible;
        opacity: 1;
    }

    .link{
        width: 60px;
        height: 60px;
        position: absolute;
        top: 55px;
        left: calc(50% - 30px);
        visibility: hidden;
        opacity: 0;
        transition: all .5s ease;
        z-index: 25;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .link .rectangular{
        background-color: white;
        /* display: flex;
        justify-content: center;
        align-items: center; */
        
    }


    .link a{
        position: relative;
        z-index: 15;
        font-size: 24px;
    }

    @media only screen and (max-width: 900px){
        .recent__works__card{
            width: 50%;
        }
    }
 
    @media only screen and (max-width: 900px){
        .recent__works__card{
            width: 100%;
        }
    }




</style>