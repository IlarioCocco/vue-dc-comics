<template>
    <main>
        <div class="load">
          <div class="box2">
            <button>load more</button>
          </div>
        </div>
        <div class="main">
            <div class="box3">
                <ul class="lista">
                    <li v-for="(link, i) in menu" :key="i">
                        <a :href="link.url" :class="{active : link.current}">
                          <img class="shop" :src="require(`@/assets/img/` + link.url)" alt="imagini shop">
                        {{link.text}}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>




<script>
export default {
  name: 'Main',
   data() {
        return {
            menu: [
                {
                  text: "digital comics",
                  url: "buy-comics-digital-comics.png",
                  current: true,
                },
                {
                  text: "dc merchandise",
                  url: "buy-comics-merchandise.png",
                  current: true,
                },
                {
                  text: "subscription",
                  url: "buy-comics-subscriptions.png",
                  current: true,
                },
                {
                  text: "comic shop locator",
                  url: "buy-comics-shop-locator.png",
                  current: true,
                },
                {
                  text: "dc power visa",
                  url: "buy-dc-power-visa.svg",
                  current: true,
                },
            ]
        }
    }
}
</script>





<style lang="scss" scoped>
.box2 {
    width: 65%;
    height: 100%;
    margin: auto;
    display: flex;
    justify-content: center;
    // border: 5px solid rgb(133, 111, 111);
    align-items: center;
    padding: 30px 0px 30px 0px;
}

.content {
  background-color: rgb(0, 0, 0);
  color: white;
  padding: 0px 0px 0px 0px; 
  display: flex;
  font-size: 12px;


}

.box3 {
  width: 65%;
  height: 100%;
  margin: auto;
  display: flex;
  justify-content: center;
  // border: 5px solid rgb(240, 84, 0);
  align-items: center;
  padding: 0px 0px 0px 0px;
}

.shop{
  width: 40px;
  display: flex;
  margin: 5px  15px  5px  15px;
  justify-content: center;
}

.main {
  background: rgb(0, 0, 0);

    a {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
    padding: 40px 55px 40px 50px;
    color: white;
    font-size: 13px;

    &.active:hover {
      color: rgb(0, 131, 254);
    }
  }
}

.lista {
  // display: flex;
  // align-items: center;
  font-size: 10px;
  text-transform:uppercase;
}

.load {
  background-color: rgb(0, 0, 0);
  color: white;
}

button {
    background-color: rgb(43, 117, 255);
    padding: 15px 45px;
    color: white;
    text-transform:uppercase;
    font-weight: bold;
    font-size: 15px;
    border: none;
    cursor: pointer;
}




// responsive
@media screen and (min-width: 1400px){
  .main {
  background: rgb(43, 117, 255);
  height: 160px;

    a {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 40px 55px 40px 50px;
    color: white;
    font-size: 13px;
    

    &.active:hover {
      color: rgb(0, 0, 0);
      padding-top: 1px;
    }
  }
}
  .lista {
    display: flex;
    align-items: center;
    font-size: 10px;
    text-transform:uppercase;
  }

  .shop{
    width: 35px;
    display: flex;
    margin: 10px  5px  10px  5px;
    justify-content: center;
  }
} 
</style>
