<template>
   <div>
       <span>{{group.groupEntry1}}</span><br>
       <span>{{group.groupEntry2}}</span><br>

   </div>
</template>

<script>
    export default {
        name: "grouped-props",
        props: {
            group: {
                type: Object,
                default: {
                    nameTopic: "default name",
                    ageTopic: "default age",
                }
            }
        }
    }
</script>

<style scoped>

</style>