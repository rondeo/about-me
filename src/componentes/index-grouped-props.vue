<template>
    <table class="table m-0 border">
        <tr class="row">
            <td class="col p-0">{{content.id}}</td>
            <td class="col p-0">{{content.groupListEntry1}}</td>
            <td class="col p-0">{{content.groupListEntry2}}</td>
            <td class="col p-0">{{content.groupListEntry3}}</td>
        </tr>
    </table>
</template>

<script>
    export default {
        name: "index-grouped-props",
        props: {
            content: {
                typ: Object,
            },
        }
    }
</script>

<style scoped>

</style>