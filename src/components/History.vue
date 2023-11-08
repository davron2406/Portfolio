<template>
    <div class="history" id="history">

        <h1 class="history__title">
            A LOOK BACK AT MY HISTORY
        </h1>
        <p class="history__subtitle">
            THIS IS MY EDUCATION AND EXPERIENCE
        </p>
        <div class="container">
            <ul class="timeline">
                <li class="timeline__start">
                    <div class="rectangular"></div>
                    <p>2009
                        2018</p>
                </li>

                <li class="timeline__simple">
                    <div class="timeline__rectangular"></div>
                    <div class="timeline__panel">
                        <div class="timeline__heading">
                            <div class="timeline__date">
                                <p>13 Sep</p>
                            </div>
                            <div class="timeline__position">
                                <p>Study at school</p>
                            </div>
                        </div>

                        <div class="timeline__body">
                            <div class="timeline__body__thumb">
                                <img src="../assets/images/school.webp" alt="">
                            </div>
                            <p>I studied at school №15 in Zarbdor</p>
                        </div>
                    </div>
                </li>

                <li class="timeline__start">
                    <div class="rectangular"></div>
                    <p>2018
                        2020
                    </p>

                </li>

                <li class="timeline__inverted">
                    <div class="timeline__rectangular__inverted"></div>
                    <div class="timeline__panel">
                        <div class="timeline__heading">
                            <div class="timeline__date">
                                <p>13 Sep</p>
                            </div>
                            <div class="timeline__position">
                                <p>Academic Lyceum</p>
                            </div>
                        </div>

                        <div class="timeline__body">
                            <div class="timeline__body__thumb">
                                <img src="../assets/images/AcademicLyceum.jpg" alt="">
                            </div>
                            <p>I studied at Academic Lyceum of Tashkent state Technical University</p>
                        </div>
                    </div>
                </li>

                <li class="timeline__start">
                    <div class="rectangular"></div>
                    <p>2020
                        2021
                    </p>

                </li>

                <li class="timeline__simple">
                    <div class="timeline__rectangular"></div>
                    <div class="timeline__panel">
                        <div class="timeline__heading">
                            <div class="timeline__date">
                                <p>13 Sep</p>
                            </div>
                            <div class="timeline__position">
                                <p>University</p>
                            </div>
                        </div>

                        <div class="timeline__body">
                            <div class="timeline__body__thumb">
                                <img src="../assets/images/University.jpg" alt="">
                            </div>
                            <p>I studied National University of Uzbekistan</p>
                        </div>
                    </div>
                </li>

                <li class="timeline__start">
                    <div class="rectangular"></div>
                    <p>2021-2022</p>

                </li>

                <li class="timeline__inverted">
                    <div class="timeline__rectangular__inverted"></div>
                    <div class="timeline__panel">
                        <div class="timeline__heading">
                            <div class="timeline__date">
                                <p>13 Sep</p>
                            </div>
                            <div class="timeline__position">
                                <p>PDP ACADEMY</p>
                            </div>
                        </div>

                        <div class="timeline__body">
                            <div class="timeline__body__thumb">
                                <img src="../assets/images/PDP.jpg" alt="">
                            </div>
                            <p>I learned programming at PDP Academy</p>
                        </div>
                    </div>
                </li>

                <li class="timeline__start">
                    <div class="rectangular"></div>
                    <p>2022-2023</p>

                </li>

                <li class="timeline__simple">
                    <div class="timeline__rectangular"></div>
                    <div class="timeline__panel">
                        <div class="timeline__heading">
                            <div class="timeline__date">
                                <p>13 Sep</p>
                            </div>
                            <div class="timeline__position">
                                <p>Intern and work</p>
                            </div>
                        </div>

                        <div class="timeline__body">
                            <div class="timeline__body__thumb">
                                <img src="../assets/images/realsoft.png" alt="">
                            </div>
                            <p>I worked at Realsoft academy </p>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
           
    </div>    
    
</template>

<style>

    .history{
        background: white;
        padding-top: 50px;
        width: 100%;
    }

    .history__title{
        text-align: center;
        color: #196fc2;
    }

    .history__subtitle{
        text-align: center;
        color: #666666;
        margin-top: 10px;
    }

    .timeline{
        list-style: none;
        position: relative;
       
    }

    .timeline::before{
        top: 0;
        bottom: 0;
        position: absolute;
        content: " ";
        width: 1px;
        background-color: #dddddd;
        left: 50%;
        margin-left: -0.5px;
        z-index: 2;
    }

    .timeline li{
        position: relative;
    }

    .timeline>li:before{
        content: "";
        display: table;
    }

    .timeline>li + li{
        margin-top: 50px;
    }
    .timeline__start{
        width: 50px;
        height: 50px;
        margin-top: 50px;
        display: flex;
        justify-content: center;
        align-items: center;

        position: relative;
        z-index: 3;
        background-color: white;
        left: calc(50% - 25px);
    }

    .timeline__start p{
        text-align: center;
    }

    .timeline .timeline__rectangular{
        position: absolute;
        margin: 0 auto;
        top: 15px;
        left: 0.5px;
        right: 0;
        background-color: #666;
        width: 20px;
        height: 20px;
        border: 0;
        z-index: 99;
        transform: rotate(45deg);
    }

    .timeline__panel{
        width: 50%;
        /* float: left; */
        border-bottom: 1px solid #d4d4d4;
        border-radius: 2px;
        position: relative;
        padding-right: 10px;
    }
    
    .timeline__panel::before{
        content:"";
        position: absolute;
        top: 15px;
        right: 0px;
        background-color: #f6f6f6;
        width: 20px;
        height: 20px;
        transform: rotate(45deg);   

    }

    .timeline__body__thumb{
        width: 200px;
    }

    .timeline__body__thumb img{
        width: 100%;
    }

    .timeline__simple{
        position: relative;
        right: 20px;
    }

    .timeline__inverted {
        width: 50%;
        position: relative;
        left: calc(50% + 40px);
    }

    .timeline__inverted .timeline__panel{
        width: 100%;
    }

    .timeline__inverted .timeline__rectangular__inverted{
        position: absolute;
        margin: 0 auto;
        top: 15px;
        left: -20px;
        /* right: 0; */
        background-color: #666;
        width: 20px;
        height: 20px;
        border: 0;
        z-index: 99;
        transform: rotate(45deg);
    }

    .timeline__inverted .timeline__panel::before{
        left: -10px;
        right: auto;
    }

    .timeline__heading{
        background-color:#666;
        line-height: 50px;
        height: 50px;
        display: flex;
    }

    .timeline__position{
        padding-left: 5px;
    }

    .timeline__date{
        padding: 0 10px;
        background-color: #196fc2;
    }

    .timeline__body{
        position: relative;
        padding: 20px 0;
        min-height: 140px;
        display: flex;
    }

    .timeline__body p{
        padding: 0 20px;
    }

    @media only screen and (max-width: 700px){
        .timeline__body{
            display: flex;
            flex-direction: column;
        }
    }
</style>