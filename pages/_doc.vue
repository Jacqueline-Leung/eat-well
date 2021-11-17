<template>
    <div>
        <NuxtContent :documment="doc" />
    </div>  
</template>

<script>

export default {

    async asyncData( { $content, params } ) {
        const doc = await $content('documentation', params.doc).fetch()
        return{doc}
    }
}
</script>

<style>

</style>