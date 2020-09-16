<template>
    <div class="container">
        <headerBlock />
        <Project />
        <Studio />
        <News />
        <Footer />
    </div>
</template>


<script>
    import headerBlock from '~/components/Header'
    import Project from '~/components/Project'
    import Studio from '~/components/Studio'
    import News from '~/components/News'
    import Footer from '~/components/Footer'

    export default {
        data: () => ({

        }),
        components: {
            headerBlock,
            Project,
            Studio,
            News,
            Footer
        }
    }
</script>

<style>

</style>