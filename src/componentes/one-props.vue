<template>
    <div class="border text-center m-0">
        <span>{{single}}</span>
    </div>
</template>

<script>
    export default {
        name: "one-props",
        props: {
            single: {
                type: String,
                default: "Vue Properties DEFAULT"
            }
        }
    }
</script>

<style scoped>

</style>