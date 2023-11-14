<template>
   <div class="background">

   </div>

  <Showcase></Showcase>
  <Intro></Intro>
  <Aim></Aim>
  <About></About>
  <Skills></Skills>
  <Services></Services>
  <Clients @next="next" @prev="prev" 
    v-bind:clients="this.clients" 
    :visibleClient="this.visibleClient"
    :direction="this.clientDirection"></Clients>
  <Team></Team>
  <History></History>
  <RecentWorks></RecentWorks>
  <Footer></Footer>

 

</template>



<script>

import Showcase from './components/Showcase.vue';
import Intro from './components/Intro.vue';
import Aim from './components/Aim.vue';
import About from './components/About.vue';
import Skills from './components/Skills.vue';
import Services from './components/Services.vue';
import Clients from './components/Clients.vue';
import Team from './components/Team.vue';
import History from './components/History.vue';
import RecentWorks from './components/RecentWorks.vue';
import Footer from './components/Footer.vue';

export default {
  components:{
    Showcase,
    Intro,
    Aim,
    About,
    Skills,
    Services,
    Clients,
    Team,
    History,
    RecentWorks,
    Footer,
  },

  data() {
            return{
                clients: [
                    {
                        clientImg : "/src/assets/images/client.jpg",
                        clientName : "Abdug'affor Malikov",
                        clientPosition : "Director at Local company",
                        clientReview : "if there were 100 star rating I would leave 110.I have been building WP sites now full time for 7 years and in business for 12 and have never worked with such a solid company with such a wonderful set of themes"
                    },
                    {
                        clientImg : "/src/assets/images/client2.jpg",
                        clientName : "Soliha Abdurashidova",
                        clientPosition : "CEO at Law firm",
                        clientReview : "Diana Johnson is a rare SEo consultant who does thing the right way. I've been consistently impressed with her process, organization and stratagic method of doing SEO the right way"
                    },

                ],
                visibleClient:0,
                clientDirection: "left",

            }
        },

        created() {

              this.clientsLength = this.clients.length;

              window.addEventListener("scroll" , function(){
                  var header = document.querySelector('.header');
                  // this.document.querySelector('.first__nav').classList.add('active__nav');
                  
                  if(window.scrollY > this.window.innerHeight){
                      header.style.position='fixed';
                      header.style.top = '0';  
                  }
                  else{
                      header.style.position ='absolute';
                  }
              })
              },

        methods: {
              next(){
                  
                  if(this.visibleClient == this.clients.length -1){
                      this.visibleClient = 0;

                  }
                  else{
                      this.visibleClient++;
                  }

                  this.clientDirection = "right";
              },

              prev(){
                  if(this.visibleClient == 0){
                      this.visibleClient = this.clients.length - 1;
                  }
                  else{
                      this.visibleClient--;
                  }

                  this.clientDirection = "left";
              }
              }
    
}


</script>
  

<style >

.background{
    width: 100vw;
    height: 100vh;
    background-image: url('./assets/images/work.jpg');
    background-position: center;
    background-size: cover;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;

}

</style>
