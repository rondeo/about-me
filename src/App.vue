<template>
    <div class="container">
        <navi-topic :language1="php"></navi-topic>
    </div>
</template>
<script>

    import NaviTopic from "./componentes/controlpanel/navi-topic";
    export default {
        name: 'app',
        components: {
            NaviTopic,
        },
        data() {
            return {
                php: {
                    name: "PHP",
                    level:"gut",
                    description:"gute Kenntnisse in der prozedualen Programmierung"
                }
            }
        }
    }
</script>

<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
    .navbar-toggler,button, button:focus, input {
        outline: none;
        border: none;
    }
</style>