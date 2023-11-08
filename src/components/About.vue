<template>
    <div class="about" id="about"> 
        <div class="about__main container">
            <h1 class="about__main__title">
                About Davron's Test Results
            </h1>

            <p class="about__main__subtitle">
                <span></span>
                Our Goal is to build products and Services
                <span></span>
            </p>

            <div class="about__main__cards">
                <div class="about__main__card">
                    <div class="about__main__card__icon">
                        <div class="rectangular">
                           
                        </div>

                        800
                    </div>

                    <div class="about__main__card__info">
                        <h2>Sat Math</h2>
                        <p>Algebra (35% of section, 13-15 questions),<br>  
                           Advanced Math (35% of section, 13-15 questions),<br>
                           Problem-Solving and Data Analysis (15% of section, 5-7 questions),<br>
                           Geometry andTrigonometry (15% of section, 5-7 questions),
                        </p>
                    </div>
                </div>

                <div class="about__main__card">
                    <div class="about__main__card__icon">
                        <div class="rectangular">
                            
                        </div>

                       600
                    </div>

                    <div class="about__main__card__info">
                        <h2>Sat English</h2>
                        <p>Information and Ideas (26% of section, 12-14 questions), <br>
                            Craft and Structure (28% of section, 13-15 questions), <br>
                            Expression ofIdeas (20% of section, 8-12 questions), <br>
                            Standard English Conventions (26% of section, 11-15 questions)

                        </p>
                    </div>
                </div>

                <div class="about__main__card">
                    <div class="about__main__card__icon">
                        <div class="rectangular">
                           
                        </div>

                        8
                    </div>

                    <div class="about__main__card__info">
                        <h2>IELTS Reading</h2>
                        <p>IELTS Band Score: 8 Skill Level: Very good. The test taker has fully operational command of the language with only occasional unsystematic inaccuracies and inappropriate usage. They may misunderstand some things in unfamiliar situations. They handle complex and detailed argumentation well.</p>
                    </div>
                </div>

                <div class="about__main__card">
                    <div class="about__main__card__icon">
                        <div class="rectangular">
                            
                        </div>

                        7
                    </div>

                    <div class="about__main__card__info">
                        <h2>IELTS Listening</h2>
                        <p>IELTS Band Score: 7 Skill Level: Good. The test taker has operational command of the language, though with occasional inaccuracies, inappropriate usage and misunderstandings in some situations. They generally handle complex language well and understand detailed reasoning.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>

    .about{
        background-color: white;
        padding-top: 100px;
        
    }

    .about__main{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .about__main h1{
        color: #196FC2;
        font-size: 48px;
        text-align: center;
    }

    .about__main p{
        margin-bottom: 60px;
        margin-top: 20px;
        display: flex;
        align-items: center;
        gap: 20px;
        color: #666666;
        font-size: 18px;
        text-align: center;
    }

    .about__main p span{
        display: inline-block;
        height: 2px;
        width: 20px;
        background-color: #666666;
    }

    .about__main__cards{
        display: flex;
        justify-content: space-between;
    }

    .about__main__card{
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 23%;
    }


    .about__main__card__icon{
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        color: red;
        font-size: 24px;

        width: 70px;
        height: 70px;
    }

    .about__main__card__info{
        margin-top: 40px;
    }

    @media only screen and (max-width: 900px){

       
        .about__main__card{
            width: 45%;
        }

        .about__main__cards{
            flex-wrap: wrap;
        }
    }


    @media only screen and (max-width: 900px){
        .about__main__card{
            width: 100%;
        }

        .about__main__card__info h2{
            font-size: 20px;
        }

        .about__main__card__info p{
            font-size: 16px;
            margin-top: 10px;
        }
    }

</style>