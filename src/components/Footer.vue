<template>
    <div class="footer">
        <div class="container">
            <div class="footer__social__media">
                <a href="https://www.instagram.com/davron.saydullayev.2406/">
                    <i class="fa fa-instagram"></i>
                </a>
                <a href="https://t.me/Saydullayev_Davron">
                    <i class="fa fa-telegram"></i>
                </a>
                <a href="https://twitter.com/DavronSaydulla5">
                    <i class="fa fa-twitter"></i>
                </a>

                <a href="https://www.facebook.com/davron.saydullayev.10">
                    <i class="fa fa-facebook"></i>
                </a>
                <a href="#https://www.youtube.com/@InBrainuz">
                    <i class="fa fa-youtube"></i>
                </a>
            </div>
        </div>
    </div>

</template>

<style>
    .footer{
        background-color: #196fc2;
        padding: 30px;
    }

    .footer__social__media{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 100px;
    }
    .footer__social__media a{
        font-size: 32px;
        color: white;
    }

    @media only screen and (max-width: 700px){
        .footer__social__media{
            gap: 30px;
        }
    }
</style>