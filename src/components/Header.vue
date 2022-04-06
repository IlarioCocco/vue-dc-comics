<template>
  <header>
    <div class="box1">
        <div>
          <img class="logo" src="../assets/img/dc-logo.png" alt="logo dc">
        </div>
        <nav>
          <ul class="lista">
            <li v-for="(link, i) in menu" :key="i">
              <a :href="link.url" :class="{active : link.current}">
                {{link.text}}
              </a>
            </li>
          </ul>
        </nav>
    </div>
  </header>
</template>




<script>
export default {
  name: 'Header',
   data() {
        return {
            menu: [
                {
                  text: "charaters",
                  url: "#",
                  current: true,
                },
                {
                  text: "comics",
                  url: "#",
                  current: true,
                },
                {
                  text: "movies",
                  url: "#",
                  current: true,
                },
                {
                  text: "tv",
                  url: "#",
                  current: true,
                },
                {
                  text: "collectibles",
                  url: "#",
                  current: true,
                },
                {
                  text: "videos",
                  url: "#",
                  current: true,
                },
                {
                  text: "fans",
                  url: "#",
                  current: true,
                },
                {
                  text: "news",
                  url: "#",
                  current: true,
                },
                {
                  text: "shop",
                  url: "#",
                  current: true,
                },
            ]
        }
    }
}
</script>





<style scoped lang="scss">
.box1 {
    width: 65%;
    height: 100%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    // border: 1px solid rgb(0, 0, 0);
    align-items: center;
    padding: 0px 0px 0px 0px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgb(255, 255, 255);
  
  

    a {
    display: inline-flex;
    padding: 50px 0px 45px 0px;
    margin: 0px 0px 0px 40px;
    text-decoration: none;
    color: black;
    border-bottom: 5px solid rgba(0, 0, 0, 0);

    &.active:hover {
      color: rgb(0, 162, 255);
      border-bottom: 5px solid  rgb(0, 162, 255);
      max-width: 100%;
    }
  }
}

.logo{
  width: 90%;
}

.lista {
  display: flex;
  list-style: none;
  font-size: 12px;
  text-transform:uppercase;
  font-weight: bold;
}
</style>
