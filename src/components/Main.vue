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
                  url: "#",
                  current: false,
                },
                {
                  text: "dc mechandise",
                  url: "#",
                  current: true,
                },
                {
                  text: "subscription",
                  url: "#",
                  current: false,
                },
                {
                  text: "comic shop locator",
                  url: "#",
                  current: false,
                },
                {
                  text: "dc power visa",
                  url: "#",
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
}

.content {
  background-color: rgb(0, 0, 0);
  color: white;
  padding: 30px 0px 30px 0px; 
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

.main {
  background: rgb(43, 117, 255);
  // display: flex;
  // justify-content: space-between;
  // align-items: center;

    a {
    display: flex;
    padding: 50px 80px 50px 80px;
    // margin:  50px 100px 50px 100px;
    color: white;

    &.active {
      color: rgb(0, 23, 54);
    }
  }
}

.lista {
  display: flex;
  font-size: 10px;
  text-transform:uppercase;
}
</style>
