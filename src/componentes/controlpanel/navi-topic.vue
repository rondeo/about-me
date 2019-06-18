<template>
    <div>
        <div class="row">
            <div class="col p-0">
                <nav class="navbar navbar-dark bg-dark">
                    <visiting-card></visiting-card>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                </nav>
            </div>
        </div>
        <div class="collapse row overflow-auto" id="navbarToggleExternalContent">
                <div class="col p-0">
                    <p-languages></p-languages>
                </div>
        </div>
    </div>
</template>
<script>
    import 'bootstrap/js/dist/collapse.js';
    import VisitingCard from "./visiting-card";
    import PLanguages from "./p-languages";
    export default {
        name: "navi-topic",
        components: {PLanguages, VisitingCard},
        data() {
            return {
            }
        }
    }
</script>

<style scoped>
    .w-max {
        max-width: 45px;
    }
</style>