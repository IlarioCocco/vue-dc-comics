<template>
  <div class="Header">
      <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="logo dc">
      </div>
      <div>
        <nav>
          <ul class="lista">
            <li>charaters</li>
            <li>comics</li>
            <li>movies</li>
            <li>tv</li>
            <li>games</li>
            <li>collectibles</li>
            <li>videos</li>
            <li>fans</li>
            <li>news</li>
            <li>shop</li>
          </ul>
        </nav>
      </div>
  </div>
</template>






<script>
export default {
  name: 'Header',
 
}
</script>






<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.Header {
    text-align: center;
    background: rgb(201, 201, 201);
    display: flex;
    justify-content: space-around;
    width: 100%;
}

.logo{
    padding: 20px;
}

.lista {
    display: inline-flex;
    padding: 10px;
    padding-left: 10px;
}
</style>
