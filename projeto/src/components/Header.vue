<template>
  <div id="header">
    <div class="navbar">
        <div class="brand-div">
        <a href="" class="brand">Logo</a>
        </div>
        <div class="search">
            <div class="search-icon-div">
                <img :src="`${dominio}/assets/search.png`" alt="" class="search-icon">
            </div>
            <input type="text" placeholder="Search Post">
        </div>
    </div>
    <div class="banner">
        <h2 class="title">
            <img :src="`${dominio}/assets/like.png`" alt="" class="icon">
            Postes Famosos
        </h2>
        <Carousel v-model="value1" loop>
            <CarouselItem>
                <div class="posts">
                    <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                </div>
            </CarouselItem>
            <CarouselItem>
                <div class="posts">
                    <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                     <div class="post">
                        <div class="img-div">
                            <img :src="`${dominio}/assets/default_img.jpg`" alt="">
                        </div>
                        <div class="post-title">
                            <p>Lorem ipsum dolor sit amet.</p>
                        </div>
                    </div>
                </div>
            </CarouselItem>
        </Carousel>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex'
export default{
  computed:{
    ...mapState(['dominio'])
  },
    data(){
        return {
            value1:0
        }
    }
}
</script>

<style lang="scss">
$orange:#ff914d;
#header{
    .navbar{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 25px;
        border-bottom: 3px solid $orange;
        .brand-div{
            padding:2.5em;
            background: $orange;
            border-radius: 50%;
        }

        .search{
            display: flex;
            align-items: center;
            margin-right: 250px;
            border-bottom:2px solid $orange;
            padding-bottom:5px;
            width: 300px;
            .search-icon-div{
                border-radius: 50%;
                background: $orange;
                padding:8px ;
                display: flex;
                align-items: center;
                justify-content: center;
                .search-icon{
                    width: 17px;
                }
            }
            input{
                background:transparent;
                outline: 0;
                border: none;
                padding: 9px 3px;
            }
        }
    }
    .banner{
        .title{
            padding:15px 20px;
            border-radius: 50%;
            background: $orange;
            display:inline-block;
            color: white;
            .icon{
                width: 22px;
            }
        }
        .posts{
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            gap: 10px;
            .post{
                position: relative;
                display: flex;
                align-items: flex-end;
                .img-div{
                    img{
                        width: 100%;
                    }
                }
                .post-title{
                    position: absolute;
                    z-index: 10;
                    padding: 10px 15px;
                    background: black;
                    opacity: .6;
                    width: 100%;
                    color: white;
                    p{
                        text-align: center;
                    }
                }
            }
        }
    }
}
</style>