<template>
    <section :style="`background-image: url(${bgImage})`" >
        <div class="box4">
            <button>current series</button>
        </div>
            
    </section>
</template>




<script>
export default {
  name: 'Jumbo',
    props: [
    'bgImage'
    ]
   
}
</script>







<style lang="scss" scoped>
section {
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
    height: 42vh;
    position: relative;
}

.box4 {
    width: 68.5%;
    height: 100%;
    margin: auto;
    position: relative;
    // border: 1px solid rgb(255, 0, 0);
}

button {
    background-color: rgb(43, 117, 255);
    padding: 15px 20px;
    color: white;
    text-transform:uppercase;
    font-weight: bold;
    font-size: 25px;
    border: none;
    cursor: pointer;
    position: absolute;
    bottom: -30px;
    z-index: 2;
}
</style>
