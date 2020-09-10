<template>
    <span v-if="false"></span>
</template>

<script>
export default {
    data: () => ({
        href: 'http://twitter.com/instent/tweer?url=' +
        encodeURIComponent('https://head-elements.now.sh/about')
    }),
    head: {
        meta: [
            { name: 'twitter:card', content: 'summary' },
            { name: 'twitter:site', content: '@nuxt_js' }
        ]
    }
}
</script>

<style>

</style>
