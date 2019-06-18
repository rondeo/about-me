<template>
    <div class="container">
        <navi-topic></navi-topic>
    </div>
</template>
<script>
    import NaviTopic from "./componentes/controlpanel/navi-topic";
    export default {
        name: 'app',
        components: {
            NaviTopic,
        }
    }
</script>

<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
    .navbar-toggler,button, button:focus, input {
        outline: none;
        border: none;
    }
    .mt-element {
        margin-top: 39px;
    }
</style>