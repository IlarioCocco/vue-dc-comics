<template>
    <main>
        <div>
            <div class="main">
                <div class="box2">
            <!--<i class="fa-solid fa-arrow-right"></i>
                    <h2 id="content">Content goes here</h2>
                <i class="fa-solid fa-arrow-left"></i> -->
                
                    <section class="container">
                        <!-- <div class="box" v-for="(todo, i) in comics" :key="i">
                            <img :src="todo.thumb" :alt="todo.series">
                            <h3 class="titolo">{{todo.series}}</h3>
                        </div> -->
                        <Comic v-for="(todo, i) in comics" :key="i" :dc="todo"/>
                    </section>
                    
                </div>
            </div>
        </div>
    </main>
</template>




<script>
import Comic from '../components/Comic.vue';
import copertine from '../data/comics';
export default {
  name: 'Comics',
  components: {
    Comic
  },
   data() {
        return {
        comics: copertine 
        }
    }
}
</script>





<style lang="scss" scoped>
.main {
    color: white;
    background-color: rgb(0, 0, 0);
    padding: 50px 0px 30px 0px;
    // display: flex;
    // justify-content: center;
    font-size: 20px;
    // border: 5px solid rgb(85, 255, 0);
}

.box2 {
    max-width: 100%;
    height: 100%;
    margin: auto;
    // border: 5px solid rgb(0, 119, 255);
}

.container {
    flex-wrap: wrap;
    display: flex;
}

// img {
//     width: 100%;
// }

// .titolo{
//     position: absolute;
//     text-transform: uppercase;
//     font-size: 14px;
//     z-index: -1;
//     text-align: center;
// }

// .box {
//     width: calc(100% / 6 - 20px);
//     margin: 10px 10px 10px 10px;
//     // width: calc(100% / 4 - 0px);
//     display: flex;
//     align-items: center;
//     justify-content: center;
//     color: white;
//     // padding: 10px 10px 10px 10px;
//     // border: 1px solid rgba(255, 255, 255, 0.205);
//     // background-color: rgba(116, 116, 116, 0);

//     position: relative;
//     clip-path: inset(0% 0% 0% 0%);
    
//     & :hover {
//         // font-size: 55px;
//         width: 95%;
//         cursor: pointer;
//         border: 1px solid rgb(255, 255, 255); 
//         transition: 0.3s;
//         opacity: 25%;
//     }
// }

// responsive
@media screen and (min-width: 1400px) {
        .box2 {
        width: 65%;
        height: 100%;
        margin: auto;
        // border: 1px solid rgb(0, 119, 255);
    }
}
</style>

