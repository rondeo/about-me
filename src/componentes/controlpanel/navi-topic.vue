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
        <div class="collapse row" id="navbarToggleExternalContent">
                <div class="col p-0">
                    <table class="row-fluid table table-hover">
                        <thead>
                        <tr class="bg-dark text-white">
                            <th scope="col">Sprache</th>
                            <th scope="col">Selbsteinschätzung</th>
                            <th scope="col">Erfahrung in Jahren</th>
                            <th scope="col">Woher kommt die Erfahrung</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <th scope="row">HTML/CSS/SCSS</th>
                            <td>Experte</td>
                            <td>19</td>
                            <td>Schulfach, Umschulungsfach, Selbststudium</td>
                        </tr>
                        <tr>
                            <th scope="row">PHP</th>
                            <td>Fortgeschritten</td>
                            <td>5</td>
                            <td>Umschulungsfach, Selbststudium</td>
                        </tr>
                        <tr>
                            <th scope="row">JavaScript</th>
                            <td>Fortgeschritten</td>
                            <td>2</td>
                            <td>Umschulungsfach, Selbststudium</td>
                        </tr>
                        <tr>
                            <th scope="row">Java</th>
                            <td>Grundkenntnisse</td>
                            <td>0,5</td>
                            <td>Studienfach, Selbststudium</td>
                        </tr>
                        <tr>
                            <th scope="row">C+</th>
                            <td>Grundkenntnisse</td>
                            <td>0,5</td>
                            <td>Studienfach</td>
                        </tr>
                        <tr>
                            <th scope="row">C#</th>
                            <td>Grundkenntnisse</td>
                            <td>0,5</td>
                            <td>Umschulungsfach, Selbststudium</td>
                        </tr>
                        </tbody>
                    </table>
                </div>
        </div>
    </div>
</template>
<script>
    import 'bootstrap/js/dist/collapse.js';
    import VisitingCard from "./visiting-card";
    export default {
        name: "navi-topic",
        components: {VisitingCard},
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