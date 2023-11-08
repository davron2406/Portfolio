<template>
    <header class="header">
        <div class="header__main">
            <div class="header__name">
                <h1>Davron</h1>
            </div>

            <ul class="header__menu"   v-bind:class="(active)?'show':'hide'">
                <li class="header__menu-item active"  @click="onClick">
                   <a href="#home">Home</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#intro">Intro</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#about">About</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#services ">Services</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#clients">Clients</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#team">Team</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#history">History</a>
                </li>
                <li class="header__menu-item" @click="onClick">
                    <a href="#works">Works</a>
                </li>
            </ul>

            <div class="menu__icon"  @click="activateMenu">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </header>
</template>

<style>
    .header{
        background-color: #196FC2;
        width: 100%;
        position: absolute;
        z-index: 250;
        top: 0;
        left: 0;
    }
    .header__main{
        display: flex;
        align-items: center;
        padding: 0;
        height: 80px;
        height: 80px;
    }

    .header__menu{
        display: flex;
        list-style: none;
        width: 75%;
        gap: 50px;
        justify-content: center;
        font-size: 22px;
        padding: 0 20px;
        transition: all .3s ease;
        /* position: fixed; */
        
    }
    .header__menu-item{
        height: 97%;
        font-size: 18px;
        display: flex;
        align-items: center;
    }

    .active{
        border-bottom: 3px solid white;
    }

    .header__menu-item a{
        color: white;
    }
    .header__name{
        width: 20%;
        text-align: end;
        font-size: 26px;
        color: white;
        background-color: #004B91;
        height: 100%;
        display: flex;
        justify-content: end;
        align-items: center;
        padding: 0 20px;
    }


    .menu__icon{
        display: flex;
        flex-direction: column;
        gap: 5px;
        display: block;
    }

    .menu__icon span{
        width: 25px;
        height: 3px;
        background: black;
    }

 
    @media only screen and (max-width: 900px){
        .header__menu{
            gap: 20px;
            font-size: 18px;
        }

        .header__name{
            font-size: 18px;
        }
    }

    @media only screen and (max-width: 700px){

        .menu__icon{
            display: flex;
        }


        .header__name{
            width: 50%;
        }

        .header__main{
            justify-content: space-between;
            padding: 0 30px 0 0;
        }

        .header__menu{
            position: absolute;
            top: 80px;
            background: #196FC2;
            /* box-shadow: 0 0 20px 10px #004B91; */
            right: 0;
            flex-direction: column;
            width: 50%;
            align-items: center;
            padding: 20px 0;
            height: calc(100vh - 80px);
        }

       

        .hide{
            transform: translateX(100%);
        }

        .show{
            transform: translateX(0);
        }

        
    }



</style>

<script>

    export default {
        components: {
            
        },

        data(){
            return{
               active: false,
            }
        },

        methods: {
            onClick(event){
                const menus = document.querySelectorAll('.header__menu-item')
                    menus.forEach(item => {
                        item.classList.remove('active')
                    })

                if(!event.target.classList.contains('active') && event.target.tagName=='LI'){
                    event.target.classList.add('active')
                }
              
                if(!event.target.parentNode.classList.contains('active')){
                    event.target.parentNode.classList.add('active')
                }    
                 
                console.log(event.target.tagName)
            },

            activateMenu(){

                if(this.active){
                    this.active=false;
                }
                else{
                    this.active = true;
                }
            },

          
        }


    }
</script>