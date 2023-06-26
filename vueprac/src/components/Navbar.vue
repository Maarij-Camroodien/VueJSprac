<template>
    <nav>
        <img class="navimg" src="https://i.postimg.cc/0yTXSFtT/download.png" alt="">
        <h2>CARZ</h2>
    <!-- <router-link to="/">CARS</router-link> -->

    </nav>
</template>

<script>
    export default {
        
    }
</script>

<style>
nav {
    background-color: black;
    color: white;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
}

nav a.router-link-exact-active {
    text-decoration: none;
    color: white;
}

nav a.router-link-exact-active:hover {
    color: darkmagenta;
}

.navimg {
    width: 4rem;
}

</style>