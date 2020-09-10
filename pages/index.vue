<template>
    <div class="container">
        <h1>Cache components!</h1>
        <p>Look at the source code and see how the timestamp is not
             reloaded before 10s after refreshing the page</p>
        <p>timestamp: {{ date }}</p>
        <!-- <nuxt-link to="/about">About page</nuxt-link> -->
    </div>
</template>

<script>
export default {
    name: 'default',
    serverCacheKey() {
        return Math.floor(Date.now()/10000)
    },
    data() {
        return {
            date: Date.now()
        }
    }
    /**
     * head: {
        title: 'Home page',
        meta:[
            {
                hid: 'descrption',
                name: 'description',
                content: 'Home page description'
            }
        ]
       }
     */  
}
</script>

<style>
.container {
    text-align: center;
    margin-top: 150px;
    font-size: 20px;
}
</style>
