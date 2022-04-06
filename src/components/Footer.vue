<template>
    <footer :style="`background-image: url(${bgImage})`" >
        <div class="footer"  >
            <div class="box4">
                <div class="boxListato">
                    <ul>
                        <h3 id="titoli">dc comics</h3>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                        <h3 id="titoli">shop</h3>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                    <ul class="ul">
                        <h3 id="titoli">dc</h3>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Adversting</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscription</a></li>
                        <li><a href="#">Talent Workshops1</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings1</a></li>
                        <li><a href="#">Stop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                    <ul>
                        <h3 id="titoli">sites</h3>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC power Visa</a></li>
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
                   <button>sign-up now!</button>
                </div>
                <div class="follow">
                    <h2 class="fol">follow us</h2>
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

        & .boxListato {
        display: flex;
        justify-content: start;
        // border: 1px solid rgb(229, 255, 0);
        align-items: top;
    }
}

footer {
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
    filter: brightness(80%);
}

ul {
    color: white;
    padding: 30px 40px 60px 0px;
    font-size: 10px;
    line-height: 20px;

        &.ul {
        padding: 30px 70px 60px 0px;
    }
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
    cursor: pointer;
}

.follow {
    color: rgb(43, 117, 255);
    text-transform:uppercase;
    display: flex;
    align-items: center;
    font-weight: bold;
    font-size: 15px;

    .fol {
        padding: 0px 20px 0px 0px; 
    }
}

.social img {
    padding: 20px 0px 20px 10px;
    cursor: pointer;
}
</style>
