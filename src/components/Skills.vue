<template>
    <div class="skills">

        <div class="skills__main container90">
            <div class="skills__video">
                <div class="skills__video__intro">
                    Introduction Video
                </div>
                <iframe width="560" height="315" src="https://www.youtube.com/embed/ma44AMXANMo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
            </div>

            <div class="skills__info">
                <h2 class="skills__info__title">
                    Skills Davron got
                </h2>

                <div class="skills__info__progress__main">
                    <div class="skills__info__progress__group">
                        <p>WEb dewelopment</p>
                        <div class="skills__info__progress">
                            <div class="skills__info__progress__bar web__development__progress__bar" role="progressbar">
                                <span class="skills__info__progress__back__text">80%</span>
                            </div>
                        </div>
                    </div>

                    <div class="skills__info__progress__group">
                        <p>Math</p>
                        <div class="skills__info__progress">
                            <div class="skills__info__progress__bar math__progress__bar" role="progressbar">
                                <span class="skills__info__progress__back__text">100%</span>
                            </div>
                        </div>
                    </div>


                    <div class="skills__info__progress__group">
                        <p>Calculus</p>
                        <div class="skills__info__progress">
                            <div class="skills__info__progress__bar calculus__progress__bar" role="progressbar">
                                <span class="skills__info__progress__back__text">90%</span>
                            </div>
                        </div>
                    </div>

                    <div class="skills__info__progress__group">
                        <p>Physics</p>
                        <div class="skills__info__progress">
                            <div class="skills__info__progress__bar physics__progress__bar" role="progressbar">
                                <span class="skills__info__progress__back__text">85%</span>
                            </div>
                        </div>
                    </div>

                    <div class="skills__info__progress__group">
                        <p>English</p>
                        <div class="skills__info__progress">
                            <div class="skills__info__progress__bar english__progress__bar" role="progressbar">
                                <span class="skills__info__progress__back__text">70%</span>
                            </div>
                        </div>
                    </div>

                

                </div>
            </div>
        </div>

        <div class="row">
            <div class="row__item">
                <div class="row__item__num">
                    <div class="rectangular"></div>
                    <div class="row__item__num__icon">
                        <i class="fa fa-rocket"></i>
                        <p>5</p>
                    </div>
                </div>

                <div class="row__item__info">
                    PROJECTS LAUNCHED
                </div>
            </div>

            <div class="row__item">
                <div class="row__item__num">
                    <div class="rectangular"></div>
                    <div class="row__item__num__icon">
                        <i class="fa fa-trophy"></i>
                        <p>15</p>
                    </div>
                </div>

                <div class="row__item__info">
                    AWARDS WON
                </div>
            </div>

            <div class="row__item">
                <div class="row__item__num">
                    <div class="rectangular"></div>
                    <div class="row__item__num__icon">
                        <i class="fa fa-paper-plane"></i>
                        <p>32</p>
                    </div>
                </div>

                <div class="row__item__info">
                    PROPOSALS SENT
                </div>
            </div>

            <div class="row__item">
                <div class="row__item__num">
                    <div class="rectangular"></div>
                    <div class="row__item__num__icon">
                        <i class="fa fa-clock-o"></i>
                        <p>945</p>
                    </div>
                </div>

                <div class="row__item__info">
                    HOURS OF WORK
                </div>
            </div>

            <div class="row__item">
                <div class="row__item__num">
                    <div class="rectangular"></div>
                    <div class="row__item__num__icon">
                        <i class="fa fa-coffee"></i>
                        <p>256</p>
                    </div>
                </div>

                <div class="row__item__info">
                    CUPS OF COFFEE
                </div>
            </div>
        </div>
       
    </div>
</template>

<style>
    .skills{
        background-color: white;
        padding: 100px 0;
    }

    .skills__main{
        display: flex;
        justify-content: space-between;
        padding: 100px 0;
    }

    .skills__info{
        width: 45%;
    }

    .skills__video__intro{
        font-size: 32px;
        font-weight: 300;
        margin-bottom: 30px;
    }

    .skills__info__title{
        margin-bottom: 30px;
        font-size: 32px;
        font-weight: 300;
    }


    .skills__info__progress{
        width: 100%;
        height: 10px;
        background-color: #666;
    }

    .skills__info__progress__main{
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .skills__info__progress__bar{
        float: left;
        width: 0%;
        height: 100%;
        background-color: blue;
        transition: width 2s;
        position: relative;
    }

    .skills__info__progress__bar::before{
       content: '';
       position: absolute;
       right: 0;
       top: -10px;
       width: 0;
       height: 0;
       border-style: solid;
       border-width: 0 15px 20px 15px;
       border-color: transparent transparent blue transparent;
       z-index: 2;
    }

    .skills__info__progress__bar::after{
        content: '';
        position: absolute;
        right: -8px;
        top: -10px;
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 0 15px 20px 15px;
        border-color: transparent transparent #f6f6f6 transparent;
        z-index: 1;
    }

    .skills__info__progress{
        margin-top: 10px;
    }

    .skills__info__progress__group p{
        font-size: 18px;
        font-size: 400;
        color: #666666;
    }

    .skills__info__progress__back__text{
        position: absolute;
        top: -28px;
        right: -5px;
    }

    .row__item__num{
        position: relative;
    }

    .row{
        display: flex;
        justify-content: space-between;
        width: 80%;
        margin: auto;
        flex-wrap: wrap;
        row-gap: 20px;

    }

    .row__item{
        width: 20%;
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 30px;
    }

    .row__item__num{
        width: 70px;
        height: 70px;
        display: flex;
        justify-content: center;
        align-items: center;
    }


    .row__item__num__icon i{
        font-size: 24px;
        margin-bottom: 5px;
    }

    .row__item__num__icon p{
        font-size: 18px;
    }

    @media only screen and (max-width: 900px){
        .skills__main{
            flex-wrap: wrap;
            gap: 30px;
        }

        .skills__info{
            width: 100%;
        }

        .skills__video{
          display: none;
        }

        .row__item__info{
            text-align: center;
        }
    }

    @media only screen and (max-width: 900px){
        .row__item__num{
            width: 40px;
            height: 40px;
        }

        .row__item{
            width: 30%;
        }

        .row__item__num__icon{
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .row__item__num__icon i{
            font-size: 16px;
        }

        .row__item__num p{
            font-size: 16px;
        }

        .row__item__info{
            font-size: 14px;
        }
    }
</style>

<script>
    export default{

        created() {
            window.addEventListener("scroll" , function(){
                

                var skills = document.querySelector('.skills')
                const space = skills.offsetTop -skills.offsetHeight;

               
                if(window.scrollY > space){
                    const web_development = this.document.querySelector('.web__development__progress__bar');
                    const math = this.document.querySelector('.math__progress__bar');
                    const calculus = this.document.querySelector('.calculus__progress__bar');
                    const physics = this.document.querySelector('.physics__progress__bar');
                    const english = this.document.querySelector('.english__progress__bar');
                    
                    web_development.style="width:80%";
                    math.style="width:100%";
                    calculus.style = "width:90%";
                    physics.style = "width:85%";
                    english.style = "width: 70%";

                }
            })
        }
    }

</script>