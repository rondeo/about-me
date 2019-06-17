<template>
    <div class="container">
        <one-props :single="single"></one-props>
        <grouped-props :group="group"></grouped-props>
        <index-grouped-props v-for="(groupListIndex, index) in groupList" :key="index" :content="groupListIndex"></index-grouped-props>
    </div>
</template>
<script>
    import GroupedProps from "./componentes/grouped-props";
    import OneProps from "./componentes/one-props";
    import IndexGroupedProps from "./componentes/index-grouped-props";
    export default {
        name: 'app',
        components: {
            IndexGroupedProps,
            OneProps,
            GroupedProps,
        },
        data() {
            return {
                single:"Vue Properties einzeln",
                group: {
                    groupEntry1: "Vue Properties 1",
                    groupEntry2: "Vue Properties 2",
                },
                groupList: [
                    {id:1, groupListEntry1:"Vue Properties 1 1", groupListEntry2: "Vue Properties 1 2", groupListEntry3: "Vue Properties 1 3"},
                    {id:2, groupListEntry1:"Vue Properties 2 1", groupListEntry2: "Vue Properties 2 2", groupListEntry3: "Vue Properties 2 3"},
                    {id:3, groupListEntry1:"Vue Properties 3 1", groupListEntry2: "Vue Properties 3 2", groupListEntry3: "Vue Properties 3 3"},
                    {id:4, groupListEntry1:"Vue Properties 4 1", groupListEntry2: "Vue Properties 4 2", groupListEntry3: "Vue Properties 4 3"},
                    {id:5, groupListEntry1:"Vue Properties 5 1", groupListEntry2: "Vue Properties 5 2", groupListEntry3: "Vue Properties 5 3"},
                    {id:6, groupListEntry1:"Vue Properties 6 1", groupListEntry2: "Vue Properties 6 2", groupListEntry3: "Vue Properties 6 3"},
                    {id:7, groupListEntry1:"Vue Properties 7 1", groupListEntry2: "Vue Properties 7 2", groupListEntry3: "Vue Properties 7 3"},
                    {id:8, groupListEntry1:"Vue Properties 8 1", groupListEntry2: "Vue Properties 8 2", groupListEntry3: "Vue Properties 8 3"},
                    {id:9, groupListEntry1:"Vue Properties 9 1", groupListEntry2: "Vue Properties 9 2", groupListEntry3: "Vue Properties 9 3"},
                    {id:10, groupListEntry1:"Vue Properties 10 1", groupListEntry2: "Vue Properties 10 2", groupListEntry3: "Vue Properties 10 3"},
                ]
            }
        },
        methods: {
            getText: function (text) {
                this.text = text[0];
            }
        }
    }
</script>

<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
</style>