<template>
    <div class="clients" id="clients">
        <h1 class="clients__title">
            CLIENT REVIEWS
        </h1>

        <p class="clients__subtitle">
            OUR CLIENTS LOVE US! READ WHAT THEY HAVE TO SAY
        </p>

        <div class="clients__main">
            <div class="client">
                <button class="client__prev" @click="prevClient">
                    <i class="fa fa-angle-left"></i>
                </button>
                
              
                    <div class="client__info" v-for="(client,index) in clients" v-show="visibleClient===index">
                        <div class="client__img">
                            <img :src= "client.clientImg"  alt="">
                        </div>

                        <div class="client__review">
                            <p>{{ client.clientReview }}</p>
                        </div>

                        <div class="client__name__position">
                            <p class="client__name">{{ client.clientName }}</p>
                            <p class="client__position">{{ client.clientPosition }}</p>
                        </div>
                    </div>  
              

                <button class="client__next" @click="nextClient()">
                    <i class="fa fa-angle-right"></i>
                </button>

            </div>
            
        </div>
    </div>

</template>

<style>
    .clients{
        background-color: white;

    }

    .clients__main{
        background-color: #196FC2;
    }

    .clients__title {
        text-align: center;
        margin-bottom: 15px;
        color: #196FC2;
    }

    .clients__subtitle{
        text-align: center;
        margin-bottom: 10px;
        color: #666666;
        font-size: 18px;
    }

    .clients__main button{
        margin: 7px 5px 0;
        position: relative;
        border: 1px solid #dddddd;
        background: #ffffff;
        width: 40px;
        height: 35px;
        transform: rotate(45deg);
        -webkit-transform: rotate(45deg);
        -moz-transform: rotate(45deg);
        -o-transform: rotate(45deg);
        -ms-transform: rotate(45deg);
        opacity: 1;
        font-size: 24px;
    }

    .clients__main{
        padding: 100px 0;
    }

    .client{
        display: flex;
        align-items: center;
        width: 80%;
        margin: auto;
        gap: 30px;
    }

    .client__info{
        text-align: center;
        width: 90%;
    }

    .client__img{
        width: 80px;
        height: 80px;
        border: 0;
        margin: 20px auto 0;
        overflow: hidden;
        box-shadow: none;
        transform: rotate(45deg);
        margin-bottom: 20px;
    }

    .client__img img{
        position: absolute;
        top: 50%;
        left: 50%;
        font-size: 22px;
        transform: translate(-50%,-50%) rotate(-45deg);
        -webkit-transform: translate(-50%,-50%) rotate(-45deg);
    }

    .client__review{
        color: white;
        font-size: 20px;
        margin-bottom: 50px;
    }

    .client__name__position{
        color: white;
    }

    .client__name{
        margin-bottom: 10px;
    }

    @media only screen and (max-width: 900px){
        .client__review{
            font-size: 18px;
        }
    }

    @media only screen and (max-width: 700px){
        .client__review{
            font-size: 14px;
        }

        .clients__main{
            padding: 50px 0;
        }
    }

</style>

<script>
    export default {
        props: {
            clients : {
                type: Array,
                required: true
            },
            visibleClient:{},
            direction: {},
        },
        data() {
            return {
                
            }   
        },

        methods:{
            nextClient(){
                this.$emit("next");
            },

            prevClient(){
                this.$emit("prev");
            }
        }


    }

</script>