<template>
   <section class="container">
        <div class="box">
            <img :src="dc.thumb" :alt="dc.series">
            <h3 class="titolo">{{dc.series}}</h3>
        </div>
    </section>
</template>









<script>
export default {
    name: "Comic",
    props: ['dc']
}
</script>







<style lang="scss" scoped>
.container {
    flex-wrap: wrap;
    display: flex;
}

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
</style>