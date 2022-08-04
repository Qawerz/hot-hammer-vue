<template>
	<div id="home">
        <BgImageCmp/>
        <div class="home__header">
            <hr/>
            <h1>Наши Изделия</h1>
            <hr/>
        </div>
        <div class="container home__main">
            <div class="nav">
                <ul>
                    <li>Люстры</li>
                    <li>Коптильные Шкафы</li>
                    <li>Грилли</li>
                </ul>
                <a class="more">Еще</a>
            </div>
            <span><hr/></span>
            <div class="list">
                <div class="product__card">1</div>
                <div class="product__card">2</div>
                <div class="product__card">3</div>
                <div class="product__card">4</div>
                <div class="product__card">5</div>
                <div class="product__card">6</div>
            </div>
        </div>
	</div>
</template>

<script>
import BgImageCmp from "@/components/BgImageCmp"
export default {
    components:{
        BgImageCmp
    }
}
</script>

<style lang="scss" scoped>
#home {
    height: 100vh;
    // background-image: url('../../public/img/mockup-photos-5nUNdLueQio-unsplash.jpg');
    filter: brightness(100%);
    // color: white;
    .home{    
        &__header{

            display: flex;
            align-items: center;
            padding-top: 5rem;
            h1{
                width: 1000px;
                font-family: 'Playfair Display';
                font-style: normal;
                font-weight: 600;
                font-size: 30px;
                line-height: 53px;
                text-align: center;
            }

            hr{
                // transform: rotate(90deg);
                width: 100%;
                height: 0px;
                margin: 1rem;
            }
        }

        &__main{
            display:flex;
            flex-direction: column;

            .nav{
                display:flex;
                justify-content: space-between;
                align-items: center;

                ul{
                    padding: 0;
                    display:flex;
                    justify-content: space-around;
                    list-style: none;

                    font-family: 'Playfair Display';
                    font-style: normal;
                    font-weight: 500;
                    font-size: 25px;
                    line-height: 43px;
                    /* identical to box height */

                    text-align: center;

                    margin: 0;
                    li{
                        padding-right: 6rem;

                    }//li

                } //ul

                a {
                    &.more {
                        font-family: 'Playfair Display';
                        font-style: normal;
                        font-weight: 500;
                        font-size: 25px;
                        line-height: 43px;
                        /* identical to box height */

                        text-align: center;

                        border: 1px solid #000;
                        padding: 0.2rem 1rem;
                        border-radius: 20px 0px;

                    } //.more

                }   // a

            } // .nav

            .list {
                display: grid;
                padding-top: 1rem;
                align-items: center;
                justify-items: center;
                grid-auto-columns: 1fr; 
                grid-template-columns: 1fr 1fr 1fr ; 
                grid-template-rows: 1fr 1fr; 
                gap: 40px 10px; 
                
                .product__card {
                    width: 253px;
                    height: 300px;
                    background-color: #ccc;
                }
            }

        } //.home_main

    } //.home

} //#home
</style>