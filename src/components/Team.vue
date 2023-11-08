<template>
    <div class="team" id="team">
        <h1 class="team__title">MEET MY TEAM</h1>
        <p class="team__subtitle">THIS IS THE TEAM THAT IS WORKING WITH ME</p>

        <div class="team__cards">
            <div class="team__card">
               <div class="team__member__info">
                    <div class="team__member__img">
                        <img src="../assets/images/client.jpg" alt="">
                    </div>

                    <div class="team__member__name">
                        Diana Johnson
                    </div>
               </div>

                <div class="team__member__fullinfo">
                    <h1 class="team__member__fullname">Dima Johnson</h1>
                    <p class="team__member__position">Web Developer</p>
                    <span></span>
                    <p>Curabitur nulla odio bibendum sit amet facilisis sed lobortis id, just Donec ollic itudin facil isis nulla. Donec eget ligula.</p>

                    <div class="team__memebr__social__media">
                        <a href="#">
                            <i class="fa fa-instagram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-telegram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-facebook"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-twitter"></i>
                        </a>
                    </div>
                </div>
            </div>

            <div class="team__card">
               <div class="team__member__info">
                    <div class="team__member__img">
                        <img src="../assets/images/client.jpg" alt="">
                    </div>

                    <div class="team__member__name">
                        Diana Johnson
                    </div>
               </div>

                <div class="team__member__fullinfo">
                    <h1 class="team__member__fullname">Dima Johnson</h1>
                    <p class="team__member__position">Web Developer</p>
                    <span></span>
                    <p>Curabitur nulla odio bibendum sit amet facilisis sed lobortis id, just Donec ollic itudin facil isis nulla. Donec eget ligula.</p>

                    <div class="team__memebr__social__media">
                        <a href="#">
                            <i class="fa fa-instagram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-telegram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-facebook"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-twitter"></i>
                        </a>
                    </div>
                </div>
            </div>

            <div class="team__card">
               <div class="team__member__info">
                    <div class="team__member__img">
                        <img src="../assets/images/client.jpg" alt="">
                    </div>

                    <div class="team__member__name">
                        Diana Johnson
                    </div>
               </div>

                <div class="team__member__fullinfo">
                    <h1 class="team__member__fullname">Dima Johnson</h1>
                    <p class="team__member__position">Web Developer</p>
                    <span></span>
                    <p>Curabitur nulla odio bibendum sit amet facilisis sed lobortis id, just Donec ollic itudin facil isis nulla. Donec eget ligula.</p>

                    <div class="team__memebr__social__media">
                        <a href="#">
                            <i class="fa fa-instagram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-telegram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-facebook"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-twitter"></i>
                        </a>
                    </div>
                </div>
            </div>

            <div class="team__card">
               <div class="team__member__info">
                    <div class="team__member__img">
                        <img src="../assets/images/client.jpg" alt="">
                    </div>

                    <div class="team__member__name">
                        Diana Johnson
                    </div>
               </div>

                <div class="team__member__fullinfo">
                    <h1 class="team__member__fullname">Dima Johnson</h1>
                    <p class="team__member__position">Web Developer</p>
                    <span></span>
                    <p>Curabitur nulla odio bibendum sit amet facilisis sed lobortis id, just Donec ollic itudin facil isis nulla. Donec eget ligula.</p>

                    <div class="team__memebr__social__media">
                        <a href="#">
                            <i class="fa fa-instagram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-telegram"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-facebook"></i>
                        </a>

                        <a href="#">
                            <i class="fa fa-twitter"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>



    .team{
        background-color: white;
        padding-top: 50px;
    }

    .team__title{
        text-align: center;
        color:#196FC2;
    }

    .team__subtitle{
        text-align: center;
        margin-top: 5px;
        margin-bottom: 20px;
        color: #666666;

    }

    .team__cards{
        display: flex;
        justify-content: space-between;
        width: 80%;
        margin: auto;
        background-color: white;
        flex-wrap: wrap;
    }
    .team__card{
        position: relative;
        width: 20%;
        height: 300px;
        transform-style: preserve-3d;
        transition: all 1s ease;
        background-color: white;
    }

    .team__card:hover{
        transform: rotateY(180deg);
    }

    /* .team__card:hover .team__member__fullinfo{
        transform: rotateY(360deg);
        z-index: 4;
    } */

    .team__member__info{
       position: absolute;
       width: 100%;
       height: 280px;
       backface-visibility: hidden;
       /* background: #196FC2;  */
       border: 1px solid #666666
    }

    .team__member__fullinfo{
        position: absolute;
        width: 100%;
        height: 280px;
        backface-visibility: hidden;
        background: #196FC2;
        transform: rotateY(180deg);
        padding: 20px;
        text-align: center;
        color: white;
    }

    
    .team__member__position{
        margin-top: 10px;
        margin-bottom: 20px;
    }

    .team__memebr__social__media{
        display: flex;
        justify-content: space-between;
        width: 80%;
        margin: auto;
        margin-top: 20px;
    }

    .team__memebr__social__media a{
        color: white;
        font-size: 24px;
    }

    .team__member__img{
        width: 100%;
        margin-bottom: 0;
    }

    .team__member__img img{
        width: 100%;
    }

    .team__member__name{
        text-align: center;
        font-size: 24px;
        background-color: white;
        margin-top: 0;
    }

    @media only screen and (max-width: 900px){
        .team__card{
            width: 45%;
            height: 350px;
        }
    }

    @media only screen and (max-width: 700px){
        .team__card{
            height: 200px;
            margin-bottom: 20px;
        }

        .team__member__fullinfo{
            height: 100%;
        }

        .team__member__fullinfo p{
            font-size: 10px;
        }

        .team__member__fullinfo h1{
            font-size: 16px;
        }

        .team__member__info{
            height: 100%;
        }
    }
</style>