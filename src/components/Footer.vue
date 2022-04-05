<template>
    <footer :style="`background-image: url(${bgImage})`" >
        <div class="footer"  >
            <div class="box4">
                <div class="boxListato">
                    <ul>
                        <h3 id="titoli">dc comics</h3>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova</li>
                        <h3 id="titoli">shop</h3>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                    </ul>
                    <ul>
                        <h3 id="titoli">dc</h3>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                    </ul>
                    <ul>
                        <h3 id="titoli">sites</h3>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                        <li>ciao 123 prova1</li>
                    </ul>
                </div>
                <div class="dc">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo dc">
                </div>
            </div>
        </div>
        <div class="footerDown">
            <div class="box5 footerDown">
                <div>
                   <button>sign-ip now!</button>
                </div>
                <div class="follow">
                    <h2>follow us</h2>
                    <div class="social">
                        <img src="../assets/img/footer-facebook.png" alt="">
                        <img src="../assets/img/footer-twitter.png" alt="">
                        <img src="../assets/img/footer-youtube.png" alt="">
                        <img src="../assets/img/footer-pinterest.png" alt="">
                        <img src="../assets/img/footer-periscope.png" alt="">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>




<script>
export default {
  name: 'Footer',
    props: [
    'bgImage'
    ]
   
}
</script>







<style lang="scss" scoped>
.box4 {
    width: 65%;
    height: 100%;
    margin: auto;
    display: flex;
    justify-content: start;
    // border: 1px solid rgb(255, 0, 0);
    align-items: center;
    position: relative;
}

.boxListato {
    display: flex;
    justify-content: start;
    // border: 1px solid rgb(229, 255, 0);
    align-items: top;
}

footer {
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
    filter: brightness(80%);
}

ul {
    color: white;
    padding: 30px 50px 60px 0px;
    font-size: 10px;
    line-height: 20px;
}

.dc {
    position: absolute;
    padding: 0px 0px 0px 0px;
    right: 0;
}

.box5 {
    width: 65%;
    height: 100%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    // border: 1px solid rgb(20, 211, 55);
    align-items: center;
    padding: 20px 0px 20px 0px;
}

.footerDown {
    background-color:  rgb(32, 32, 32);
    z-index: 1;
    position: relative;
    display: flex;
    justify-content: space-between;
    color: white;
}

button {
    background-color: rgb(32, 32, 32);
    border: 1.5px solid rgb(43, 117, 255);
    padding: 15px;
    color: white;
    text-transform:uppercase;
    font-weight: bold;
    font-size: 15px;
}

.follow {
    color: rgb(43, 117, 255);
    text-transform:uppercase;
    display: flex;
    align-items: center;
    font-weight: bold;
    font-size: 15px;
}

.social img {
    padding: 10px 0px 10px 10px;
}
</style>
