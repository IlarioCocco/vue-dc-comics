<template>
    <main>
        <div>
            <h2 class="content">
                <div class="box2">
                  <i class="fa-solid fa-arrow-right"></i>
                    <h2 id="content">Content goes here</h2>
                  <i class="fa-solid fa-arrow-left"></i>
                </div>
            </h2>
        </div>
        <div class="main">
            <div class="box3">
                <ul class="lista">
                    <li v-for="(link, i) in menu" :key="i">
                        <a :href="link.url" :class="{active : link.current}">
                          <img class="shop" :src="require(`@/assets/img/` + link.url)" alt="">
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
                  current: false,
                },
                {
                  text: "dc merchandise",
                  url: "buy-comics-merchandise.png",
                  current: true,
                },
                {
                  text: "subscription",
                  url: "buy-comics-subscriptions.png",
                  current: false,
                },
                {
                  text: "comic shop locator",
                  url: "buy-comics-shop-locator.png",
                  current: false,
                },
                {
                  text: "dc power visa",
                  url: "buy-dc-power-visa.svg",
                  current: false,
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
    justify-content: flex-start;
    // border: 1px solid rgb(255, 255, 255);
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
  // border: 1px solid rgb(240, 176, 0);
  align-items: center;
  padding: 0px 0px 0px 0px;
}

.shop{
  width: 40px;
  display: flex;
  margin: 0px  20px  0px  0px;
}

.main {
  background: rgb(43, 117, 255);

    a {
    display: flex;
    align-items: center;
    padding: 40px 55px 40px 50px;
    color: white;

    &.active {
      color: rgb(0, 23, 54);
    }
  }
}

.lista {
  display: flex;
  align-items: center;
  font-size: 10px;
  text-transform:uppercase;
}
</style>
