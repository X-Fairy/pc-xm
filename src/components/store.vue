<template>
    <div class="store">
        <!-- 头部 -->
        <Header tab='4'></Header>
        <div class="main">
            <div class="linear"></div>
            <div class="floor1">
                <div class="info">
                    <div class="content">
                        <h4>STORE IMAGE UPGRADE</h4>
                        <h1>全新店面升级</h1>
                        <p class="line"></p>
                        <P class="txt" style="margin-bottom: 30px;">熙美诚品全新店铺形象，以北欧风为基调，空间色彩采用马尔斯绿，视觉统一；在产品的陈列上，从颜色、质感、款式等方面匹配货柜设计，高低组合、错落有致，让每款产品出现在最合适的位置上，从细节上体现品牌对完美和高品质的追求，给顾客带来舒适的视觉感受和购物体验。</P>
                        <P class="txt">在产品的陈列上，全新的货柜设计，高低组合错位，从颜色、质感、款式上让每件产品出现在最合适的位置上，
                                细节上体现品牌对完美和高品质的追求，给顾客带来视觉上的冲击以及最舒适的产品体验。</P>
                    </div>
                    <div class="banner">
                        <Carousel autoplay v-model="value" :autoplay-speed="5000">
                            <CarouselItem>
                                <div class="demo-carousel"><img src="@/assets/images/store/1.jpg" alt=""></div>
                            </CarouselItem>
                            <CarouselItem>
                                <div class="demo-carousel"><img src="@/assets/images/store/1.png" alt=""></div>
                            </CarouselItem>
                            <CarouselItem>
                                <div class="demo-carousel"><img src="@/assets/images/store/2.png" alt=""></div>
                            </CarouselItem>
                        </Carousel>
                    </div>
                </div>
                <img src="@/assets/images/store/2.jpg" alt="">
            </div>
            <div class="floor2">
                <h4>STORE IMAGE UPGRADE</h4>
                <h1>店面展示</h1>
                <p class="line"></p>
                <img src="@/assets/images/store/3.jpg" alt="">
            </div>
        </div>
        <BackTop :height="110" :bottom="100">
            <div class="top">
                <img src="@/assets/images/top.png" alt="">
            </div>
        </BackTop>
        <Footer></Footer>
    </div>
</template>
<script>
import Footer from './footer.vue'
import Header from './header.vue'
    export default{
        components: {
            Header,
            Footer,
        },
        data(){
            return{
                value:0
            }
        },
        methods:{}
    }
</script>