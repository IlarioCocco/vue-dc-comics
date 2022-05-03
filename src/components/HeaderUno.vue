<template>
  <header>
    <div class="box1">

        <div class="header">
            <img class="logo" src="../assets/img/dc-logo.png" alt="logo dc">
                <input class="menu-btn" id="menu-btn" type="checkbox">
                <label for="menu-btn" class="menu-icon">
                    <span class="nav-icon"></span>
                </label>
        
            <ul class="menu">
                <li v-for="(link, i) in menu" :key="i">
                    <a :href="link.url" :class="{active : link.current}">
                    {{link.text}}
                    </a>
                </li>
            </ul>
            
        </div>

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
                  url: "https://www.dccomics.com/characters",
                  current: true,
                },
                {
                  text: "comics",
                  url: "https://www.dccomics.com/comics",
                  current: true,
                },
                {
                  text: "movies",
                  url: "https://www.dccomics.com/movies",
                  current: true,
                },
                {
                  text: "tv",
                  url: "https://www.dccomics.com/tv",
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
    width: 100%;
    margin: auto;
    border: 1px solid rgb(0, 217, 255);
    padding: 0px 0px 0px 0px;
    position: fixed ;
    background-color: #000000;
    z-index: 5;
}

.header {
    background-color: #5e5e5e00;
    // box-shadow: 1px 1px 4px 0 rgb(255, 0, 0);
    position: relative;
    width: 100%;
    margin: auto;
    z-index: 5;
    // display: flex;
    // border: 1px solid rgb(255, 0, 0);
    overflow: hidden;
}

.header ul {
    overflow: hidden;
    background-color: #21212100;
}

.header ul a {
    display: flex;
    padding: 10px;
    // border-right: 1px solid rgb(51, 255, 0);
}

.header ul a:hover {
    background-color: #181818;
    color: rgb(0, 153, 255);
}

.logo {
    display: flex;
    justify-content: flex-start;
    // float: left;
    max-width: 100%;
    padding: 10px 10px;
   
}

.menu {
    max-height: 0px;
    transition: max-height .2s ease-out;
}

.menu-icon {
    // border: 1px solid rgb(255, 230, 0);
    padding: 60px 30px;
    display: flex;
    position: absolute;
    right: 0px;
    top: 0px;
    cursor: pointer;
}

.nav-icon {
    background-color: rgb(175, 175, 175);
    // display: block;
    display: flex;
    width: 20px;
    height: 3px;
    position: relative;
    transition: background-color .2s ease-out;
}

.nav-icon::before,
.nav-icon::after {
    content: "";
    // display: block;
    display: flex;
    height: 100%;
    width: 100%;
    position: absolute;
    transition: background-color .2s ease-out;
}

.nav-icon::before {
    top: 8px;
    background-color: rgb(175, 175, 175);
}

.nav-icon::after {
    top: -8px;
    background-color: rgb(175, 175, 175);
}

.menu-btn {
    display: none;
}

.header .menu-btn:checked ~ .menu {
    max-height: 400px;
}

.menu-btn:checked ~ .menu-icon .nav-icon {
    background-color: transparent;
}

.menu-btn:checked ~ .menu-icon .nav-icon::before {
    transform: rotate(-45deg);
    background-color: rgb(255, 255, 255);
    top: 0;
}


.menu-btn:checked ~ .menu-icon .nav-icon::after {
    transform: rotate(45deg);
    background-color: rgb(255, 255, 255);
    top: 0;
}


// responsive
@media screen and (min-width: 1330px){
    .box1 {
        display: none;
    }

    .header li {
        display: inline-flex;
        align-items: center;
    }

    .menu {
        display: flex;
        align-items: center;
    }
}
</style>
