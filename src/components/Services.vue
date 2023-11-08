<template>
    <div class="services" id="services">
        <div class="services__main">
            <h1 class="services__main__title">SERVICES WE DID</h1>
            <p class="services__main__subtitle">Exceptional level of service</p>

            <div class="services__menu">

                <div class="item__control">
                    <button class="prev" @click="prev"><i class="fa fa-angle-left " @click="prev"></i></button>
                    <button class="next"  @click="next"><i class="fa fa-angle-right " @click="next"></i></button>
                </div>

                <div class="services__nav">
                    <div class="services__nav__item active__nav" :index="0" @click="activateNav">
                        <div class="services__nav__item__icon">
                            <div class="rectangular rectangular__nav" ></div>
                            <i class="fa fa-laptop"></i>
                        </div>
                        <p>SUBJECT OLYMPIADS</p>
                    </div>

                    <div class="services__nav__item" :index="1" @click="activateNav">
                        <div class="services__nav__item__icon">
                            <div class="rectangular rectangular__nav" ></div>
                            <i class="fa fa-code"></i>
                        </div>
                        <p>MATH TUTOR</p>
                    </div>

                    <div class="services__nav__item" :index="2" @click="activateNav">
                        <div class="services__nav__item__icon">
                            <div class="rectangular rectangular__nav"></div>
                            <i class="fa fa-mobile-phone"></i>
                        </div>
                        <p>VOLUNTEERING</p>
                    </div>

                    <div class="services__nav__item" :index="3" @click="activateNav">
                        <div class="services__nav__item__icon">
                            <div class="rectangular rectangular__nav"></div>
                            <i class="fa fa-search"></i>
                        </div>
                        <p>EDUCATION</p>
                    </div>

                    <div class="services__nav__item" :index="4" @click="activateNav">
                        <div class="services__nav__item__icon">
                            <div class="rectangular rectangular__nav"></div>
                            <i class="fa fa-twitter"></i>
                        </div>
                        <p>SOCIAL MEDIA</p>
                    </div>
                </div>
            </div>


            <Slide v-for="(slide,index) in slides" 
            v-bind:slide="slide"
            :index="index"
            :visibleSlide="visibleSlide"
            :direction="direction"></Slide>
            
        </div>
    </div>
</template>


<style>
    .services{
        background-color: white;
        padding: 100px 0;
    }

    .services__nav{
        display: flex;
        justify-content: space-between;
        width: 80%;
        margin: auto;
        margin-top: 50px;
        height: 200px;
        border-bottom: 2px solid #196FC2;
    }

    .services__nav__item{
        width: 20%;
        padding: 30px 0;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    .services__nav__item p{
        text-align: center;
        margin-top: 30px;
        transition: all 0.5s;
    }

    


    .services__nav__item__icon{
        position: relative;
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: all 0.5s;
    }

    .services__nav__item__icon i{
        font-size: 32px;
        z-index: 15;
        transition: all 0.5s;
    }

    .active__nav{
        background-color: #196FC2;
        transition: all 0.5s;
        position: relative;
    }

    .active__nav .services__nav__item__icon{
        width: 80px;
        height: 80px;
    }

    .active__nav:after{
        content: '';
        position: absolute;
        left: 0;
        right: 0;
        bottom: -18px;
        margin: 0 auto;
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 10px 15px 0 15px;
        border-color: #196fc2 transparent transparent transparent;
        z-index: 99;
    }

    .active__nav p{
        display: none;
    }

    .active__nav .rectangular{
        box-shadow: none;
    }

    .rectangular__nav{
        background-color: white;
    }

    .item__control{
        display: flex;
        justify-content: center;
        gap: 5px;
    }

    .item__control button{
        margin: 7px 5px 0;
        position: relative;
        border: 1px solid #dddddd;
        background: #ffffff;
        width: 40px;
        height: 40px;
        transform: rotate(45deg);
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        -ms-transform: rotate(45deg);
        opacity: 1;
        font-size: 24px;
    }

    .next:hover{
        background-color: #196FC2;
    }

    .prev:hover{
        background-color: #196FC2;
    }

    .fa-angle-left::before{
        content: "\f104";
        position: absolute;
        top: 20%;
        left: 30%;
        transform: rotate(-45deg);
    }

    .fa-angle-right::before{
        content: "\f105";
        position: absolute;
        top: 10%;
        left: 43%;
        transform: rotate(-45deg);
    }

   .services__main h1{
        text-align: center;
        font-weight: 400;
        margin-bottom: 10px;
   }

   .services__main p{
        text-align: center;
        font-size: 20px;
        color: #666666;
        margin-bottom: 20px;
   }


   @media only screen and (max-width: 900px){
        .services__nav__item__icon{
            width: 40px;
            height: 40px;
        }

        .services__nav__item__icon i{
            font-size: 24px;
            
        }

        .active__nav .services__nav__item__icon{
            width: 60px;
            height: 60px;
        }

       

        .services__nav__item p{
           font-size: 16px;
           text-transform: lowercase;
           margin-top: 20px;
        }
   }

   @media only screen and (max-width: 900px){
    .services__nav{
        display: none;
    }

    
    }
</style>


<script>
import Slide from './Slide.vue';
    export default {

        components: {
            Slide,
        },

        data() {
            return {
                slides: [
                   {
                    slideTitle: "SUBJECT OLYMPIAD",
                    slideInfo: "We organized several olympiads for schoolchildren to rise their interests for education. This is a scene from Math Olympiad we did",
                    slideImg : "/src/assets/images/olympiad.jpg"
                   },
                  
                   {
                    slideTitle: "MATH TUTOR",
                    slideInfo: "I helped my teacher to teach my classmates when I was studyin academic lyceum. And Sometimes I teach after lessons until nights. Sometimes I substitude my teacher. This is scsne when I substitude my teacher ",
                    slideImg :  "/src/assets/images/lyceum.jpg"
                   },

                   {
                    slideTitle: "VOLUNTEERING",
                    slideInfo: "We have a team which helps people. We clean cameteries, mosques, even houses of disabled people, built homes for people who are young and lost their parents, and take care childrens who live in orphanage  ",
                    slideImg :  "/src/assets/images/volunterHouse.jpg"
                   },
                   {
                    slideTitle: "EDUCATION",
                    slideInfo: "we were volunteer at the company called INBRAIN. This company offer online lessons for every student to study every subject. We work on math section. This is a team I worked with.",
                    slideImg :  "/src/assets/images/inbrain.jpg"
                   },

                   {
                    slideTitle: "SOCIAL MEDIA",
                    slideInfo: "Decorations don’t drive home messages. Content does. Reducing text-based content to a visual design element (the shape of the text) can result in bloated and unrealistic client expectations once real data replaces the dummy content. We allow our design decisions to be dictated by the on-page content and messaging, and often our designers use the actual content to inspire interesting elements that might not have been conceived without it",
                    slideImg :  "/src/assets/images/web-design.jpg"
                   },
                     
                     

                ],
                visibleSlide : 0,
                direction: 'left',
                activeNav: 0,
            }

        },
        methods: {

            activateNav(event){
                const index = +event.target.getAttribute('index');
              this.deActivateNavs();
              const target =  event.target;
              if(target.classList.contains('services__nav__item')){
                target.classList.add("active__nav");
                if(index > this.visibleSlide){
                    this.direction = "left"; 
                }

                else{
                    this.direction = "right";
                }
                this.visibleSlide = index;
              }
            },

            deActivateNavs(){
            const navs = document.querySelectorAll('.services__nav__item');

            navs.forEach((item) =>  {
                item.classList.remove('active__nav');
            })
            },

            next(){

                const navs = document.querySelectorAll(".services__nav__item");

                navs.forEach((item) => {
                    const index = +item.getAttribute("index");

                    if(this.activeNav == index){
                        item.classList.remove("active__nav");
                    }

                    if(this.activeNav + 1 == index){
                        item.classList.add('active__nav');
                    }

                    if(this.activeNav + 1 == navs.length && index == 0){
                        item.classList.add("active__nav");
                    }
                })

                if(this.activeNav == navs.length - 1){
                    this.activeNav = 0;
                }

                else{
                    this.activeNav++;
                }

             
                if(this.visibleSlide >= this.slides.length - 1){
                    this.visibleSlide = 0;
                }
                else{
                    this.visibleSlide++;
                }

                this.direction = 'left';

             

               
            },

            prev(){

                const navs = document.querySelectorAll(".services__nav__item");

                navs.forEach((item) => {
                    const index = +item.getAttribute("index");

                    if(this.activeNav == index){
                        item.classList.remove("active__nav");
                    }

                    if(this.activeNav - 1 == index){
                        item.classList.add('active__nav');
                    }

                    if(this.activeNav == 0 && index == navs.length - 1){
                        item.classList.add("active__nav");
                    }
                })

                if(this.activeNav == 0){
                    this.activeNav = navs.length - 1;
                }

                else{
                    this.activeNav--;
                }

            
                if(this.visibleSlide <= 0){
                    this.visibleSlide = this.slides.length - 1;
                }
                else{
                    this.visibleSlide--;
                }
                this.direction = 'right';
               
            }

        },

    }

</script>