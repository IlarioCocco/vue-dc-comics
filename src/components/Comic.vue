<template>
    <div class="box" >
            <img :src="dc.thumb" :alt="dc.series">
            <h3 class="titolo">{{dc.series}}</h3>
    </div>
</template>




<script>
export default {
    name: "Comic",
    props: ['dc']

}
</script>





<style lang="scss" scoped>
img {
    width: 100%;
}

.titolo{
    position: absolute;
    text-transform: uppercase;
    font-size: 14px;
    z-index: -1;
    text-align: center;
}

.box {
    // width: calc(100% / 6 - 20px);
    margin: 5px 5px 5px 5px;
    width: calc(100% / 2 - 10px);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    // padding: 10px 10px 10px 10px;
    // border: 5px solid rgb(0, 213, 255);
    // background-color: rgba(116, 116, 116, 0);
    position: relative;
    clip-path: inset(0% 0% 0% 0%);
    
    & :hover {
        // font-size: 55px;
        width: 95%;
        cursor: pointer;
        border: 5px solid rgb(255, 255, 255); 
        opacity: 35%;
    }
}

// responsive 580
@media screen and (min-width: 580px){
    .box {
        width: calc(100% / 4 - 20px);
        margin: 10px 10px 10px 10px;
        // width: calc(100% / 4 - 0px);
    }
}

// responsive 1400
@media screen and (min-width: 1400px){
    .box {
        width: calc(100% / 6 - 20px);
        margin: 10px 10px 10px 10px;
        // width: calc(100% / 4 - 0px);
    }
}
</style>