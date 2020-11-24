<template>
    <div class="visual-slide">
        <v-img :src="imgSrc1" max-height="650px"></v-img>
        <div class="main-copy">
            <p class="copy"><v-img :src="imgSrc2"></v-img></p>
            <p class="big-font">Brilliant  tales  G<br>이야기의 세계로 건너가는 방법</p>
            <v-row align="center">
                <v-col>
                <v-btn outlined color="white" class="btn service">서비스 소개</v-btn>
                <v-btn outlined color="white" class="btn look-around">둘러보기</v-btn>
                <v-btn outlined color="white" class="btn login">로그인</v-btn>
                </v-col>
            </v-row>

        </div>
        <div class="visual-book-slide">
                <div>
                    <p>
                        <v-img :src="viSrc1" max-width="300" class="visual-shadow img-1"></v-img>
                        <span class="big-font">“옛날 옛적 한 소녀가 호랑이 등에 올라타 바다를 건너오니 <br>그 섬에도 그리하여 범의 자식들이 살게 됐도다.”</span>
                    </p>
                </div>
                <div>
                    <p>
                        <v-img :src="viSrc2" max-width="300" class="visual-shadow img-2"></v-img>
                        <span class="big-font">“옛날 옛적 한 소녀가 호랑이 등에 올라타 바다를 건너오니 <br>그 섬에도 그리하여 범의 자식들이 살게 됐도다.”</span>
                    </p>
                </div>
                <div>
                    <p>
                        <v-img :src="viSrc3" max-width="300" class="visual-shadow img-3"></v-img>
                        <span class="big-font">“옛날 옛적 한 소녀가 호랑이 등에 올라타 바다를 건너오니 <br>그 섬에도 그리하여 범의 자식들이 살게 됐도다.”</span>
                    </p>
                </div>
        </div>
    </div>
</template>

<script>
    import $ from 'jquery';

    export default {
        name:'VisualSlide',
        data() {

            return {
            imgSrc1:"https://britg.kr/wp-content/uploads/britg/mainbanner-bg-2.jpg?ver=0610",
            imgSrc2:"https://britg.kr/wp-content/themes/britg/img/mainbanner-logo.png?ver=0619",
            viSrc1:"http://goldenbough.minumsa.com/wp-content/uploads/bookcover/%EC%98%A4%EC%A7%81-%EB%8B%AC%EB%8B%98%EB%A7%8C%EC%9D%B4_%ED%91%9C1_%EC%9B%B9%EC%9A%A9-big-300x438.jpg",
            viSrc2:"http://goldenbough.minumsa.com/wp-content/uploads/bookcover/%ED%91%9C1_%EC%9B%B9%EC%9A%A9-300x440.jpg",
            viSrc3:"http://goldenbough.minumsa.com/wp-content/uploads/bookcover/%EA%B3%BC%EC%99%B8%ED%99%9C%EB%8F%99_%ED%91%9C1_%EC%9B%B9%EC%9A%A9big-300x468.jpg"
            };
        },
        mounted() {
            $('.visual-book-slide').slick({
            autoplay: true,
            dots: true,
            infinite: true,
            speed: 500,
            fade: true,
            cssEase: 'linear'
            });
        }
    }

</script>

<style lang="scss" scoped>
        .big-font{
            font-size: 18px;
            color: #9e9da7;
        }
.visual-slide{
    position: relative;
    .main-copy{
        position: absolute;
        top: 50px;
        left: 20%;
        .btn{
            display: block;
            margin-top: 10px;
            &:first-child{
                margin-top: 45px;
            }
        }
    }
    .visual-book-slide{
        position: absolute;
        top: 50px;
        right: 20%;
        text-align: center;
        .visual-shadow{
            box-shadow: 12px 5px 20px 1px;
        }
        span{
            display: block;
            margin-top: 20px;
        }
    }
}
</style>