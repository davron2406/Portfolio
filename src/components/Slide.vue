<template>
   
    <div class="services__contents">
        <transition :name="direction" mode="in-out">
            <div class="services__content" v-show="visibleSlide===index">
               <slot>
                <div class="content__info">
                    <h1 class="content__info__title">{{ slide.slideTitle }}</h1> 
                    <h2 class="content__info__p">{{ slide.slideInfo }}</h2>
                </div>

                <div class="content__img">
                    <img :src= "slide.slideImg" alt="">
                </div>
               </slot>
            </div>
        </transition>
    </div>



</template>

<style>
.services__contents{
    margin-top: 80px;
}

.services__content{
    display: flex;
    width: 80%;
    margin: auto;
    justify-content: space-between;
    align-items: center;
}

.content__img{
    width: 45%;
}

.content__img img{
    width: 100%;
}

.content__info{
    width: 45%;
}

.content__info h2{
    font-weight: 300;
    font-size: 20px;
}

.left-enter-active{
    animation: leftInAnimation 0.4s ease-in-out;
}

.left-leave-active{
    animation: leftOutAnimation 0.4s ease-in-out
}

@keyframes leftInAnimation{
    from{
        transform: translateX(100%);
    }

    to{
        transform: translateX(0);
    }
}

@keyframes leftOutAnimation{
    from{
        transform: translateX(0);
    }

    to{
        transform: translateX(-100%);
    }
}

.right-enter-active{
    animation: rightInAnimation 0.4s ease-in-out;
}

.right-leave-active{
    animation: rightOutAnimation 0.4s ease-in-out
}

@keyframes rightInAnimation{
    from{
        transform: translateX(-100%);
    }

    to{
        transform: translateX(0);
    }
}

@keyframes rightOutAnimation{
    from{
        transform: translateX(0);
    }

    to{
        transform: translateX(100%);
    }
}

@media only screen and (max-width: 900px){
    .content__info__title{
        font-size: 24px;
    }

    .content__info h2{
        font-size: 18px;
    }
}

@media only screen and (max-width: 700px){
    .content__info h2{
        font-size: 16px;
        text-align: center;
    }

    .services__content{
        flex-direction: column-reverse;
    }

    .content__info{
        width: 100%;
    }

    .content__img{
        width: 100%;
    }
}

</style>

<script>

export default {
    props: {
        slide: {
            type: Object,
            required: true,
        },
        visibleSlide: {},
        index: {},
        direction: {},
    },

    data() {
        return{

        }
    }
}

</script>