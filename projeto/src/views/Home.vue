<template>
  <div id="home">
    <h2 class="title">
        Postes recentes
    </h2>

    <div class="posts">
      <div class="post">
        <div class="img-div">
          <img :src="`${dominio}/assets/default_img.jpg`" alt="">
        </div>
        <div class="content">
          <h2>Titulo</h2>
          <p>Um pequeno texto dando introdução a noticia</p>
        </div>
      </div>
      <div class="post">
        <div class="img-div">
          <img :src="`${dominio}/assets/default_img.jpg`" alt="">
        </div>
        <div class="content">
          <h2>Titulo</h2>
          <p>Um pequeno texto dando introdução a noticia</p>
        </div>
      </div>
      <div class="post">
        <div class="img-div">
          <img :src="`${dominio}/assets/default_img.jpg`" alt="">
        </div>
        <div class="content">
          <h2>Titulo</h2>
          <p>Um pequeno texto dando introdução a noticia</p>
        </div>
      </div>
    </div>
    

  </div>
</template>

<script lang="ts">
import {mapState} from 'vuex'
export default{
  computed:{
    ...mapState(['dominio'])
  }
}
</script>

<style lang="scss">
$blue:#5271ff;
#home{
  margin-top:18px;
  border-top:3px solid $blue;
  .title{
    padding:15px 20px;
    border-radius: 50%;
    background: $blue;
    display:inline-block;
    color: white;
  }
  .posts{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap:1em;
    
    .post{
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid white;
      box-shadow: 0px 0px 1px 0px black;
      &:hover .img-div{
        display: block;
        cursor: pointer;
        opacity: .4;
      }
      .img-div{
        z-index: 10;
        img{
          width: 100%;
        }
      }
      .content{
        position: absolute;
        h2{
          font-size:3em;
          text-align: center;
          color: $blue;
        }
        p{
          color: black;
          font-size:1.1em;
        }
      }
    }
  }
}
</style>