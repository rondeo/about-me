<template>
    <tr>
        <th scope="row">{{skills.name}}</th>
        <td>{{skills.selfRating}}</td>
        <td>{{skills.years}}</td>
        <td>{{skills.fount}}</td>
    </tr>
</template>

<script>
    export default {
        name: "p-languages-tabline",
        props: {
            skills: {
                type: Object
            }
        }
    }
</script>

<style scoped>

</style>