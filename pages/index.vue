<template>
    <h1>  </h1>
    <div class="menu">
        <div class="test">
            <nuxt-link to="https://github.com/paulpomaret"></nuxt-link>
            <a test = "image" href="https://github.com/paulpomaret" target="_blank"><img src="https://avatars.githubusercontent.com/u/113979787?v=4"></a>
    </div>
    </div>
    <div class="mainBox">
    <h1>Mon Portfolio</h1>
    <li v-for="project in projects" :key="project.name">
        {{project.name}}
    </li>
    </div>
</template>

<style scoped>

.menu {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    background-color: rgb(37, 79, 84);
    width: 100%;
    height: 60px;
}
.test {
    display:flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 60px;
    background-color: rgb(255, 191, 0);
    background-image: url("https://avatars.githubusercontent.com/u/113979787?v=4");
    background-size: cover;
    
}

.mainBox {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 100vh;
    color:rgb(0, 0, 0);
    background-image: url("https://images6.alphacoders.com/456/456498.jpg");

}
a {
    text-decoration: underline;
}
</style>

<script setup>
const {data : projects} = await useFetch('/api/404')
</script>