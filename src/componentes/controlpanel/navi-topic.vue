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
                degQuarterList: {
                    degQuarterStart: 0,
                    degQuarter1: 0,
                    degQuarter2: 0,
                    degQuarter3: 0,
                    degQuarter4: 0,
                    degQuarter5: 0,
                    degQuarter6: 0,
                    degQuarter7: 0,
                    degQuarter8: 0,
                },
                textQuarterList: {
                    textQuarter1: "",
                    textQuarter2: "",
                    textQuarter3: "",
                    textQuarter4: "",
                    textQuarter5: "",
                    textQuarter6: "",
                    textQuarter7: "",
                    textQuarter8: "",
                },
            }
        },
        methods: {
            resetDegree: function(degree){
                if(parseInt(degree) <=25){
                    return 0;
                }
                else {
                    return parseInt(degree) -25;
                }
            },
            degSum: function() {
              return parseInt(this.degQuarterList.degQuarter1)+parseInt(this.degQuarterList.degQuarter2)+parseInt(this.degQuarterList.degQuarter3)+parseInt(this.degQuarterList.degQuarter4)+parseInt(this.degQuarterList.degQuarter5)+parseInt(this.degQuarterList.degQuarter6)+parseInt(this.degQuarterList.degQuarter7)+parseInt(this.degQuarterList.degQuarter8);
            },
            setDegree: function () {
                // ||this.degSum()<100
                if(this.degSum()>100){
                    alert("DER GESAMTWERT LIEGT ÜBER 100%");
                }
                else {
                    this.degQuarterList.degQuarterStart = parseInt(this.degQuarterList.degQuarterStart);
                    this.degQuarterList.degQuarter1 = this.resetDegree(this.degQuarterList.degQuarter1) + parseInt(this.degQuarterList.degQuarterStart);
                    this.degQuarterList.degQuarter2 = parseInt(this.degQuarterList.degQuarter2) + parseInt(this.degQuarterList.degQuarter1);
                    this.degQuarterList.degQuarter3 = parseInt(this.degQuarterList.degQuarter3) + parseInt(this.degQuarterList.degQuarter2);
                    this.degQuarterList.degQuarter4 = parseInt(this.degQuarterList.degQuarter4) + parseInt(this.degQuarterList.degQuarter3);
                    this.degQuarterList.degQuarter5 = parseInt(this.degQuarterList.degQuarter5) + parseInt(this.degQuarterList.degQuarter4);
                    this.degQuarterList.degQuarter6 = parseInt(this.degQuarterList.degQuarter6) + parseInt(this.degQuarterList.degQuarter5);
                    this.degQuarterList.degQuarter7 = parseInt(this.degQuarterList.degQuarter7) + parseInt(this.degQuarterList.degQuarter6);
                    this.degQuarterList.degQuarter8 = parseInt(this.degQuarterList.degQuarter8) + parseInt(this.degQuarterList.degQuarter7);
                    this.$emit('getInputContent',[this.degQuarterList.degQuarterStart, this.degQuarterList.degQuarter1, this.degQuarterList.degQuarter2, this.degQuarterList.degQuarter3,this.degQuarterList.degQuarter4,this.degQuarterList.degQuarter5,this.degQuarterList.degQuarter6,this.degQuarterList.degQuarter7,this.degQuarterList.degQuarter8])
                    this.degQuarterList.degQuarter8 = parseInt(this.degQuarterList.degQuarter8) - parseInt(this.degQuarterList.degQuarter7);
                    this.degQuarterList.degQuarter7 = parseInt(this.degQuarterList.degQuarter7) - parseInt(this.degQuarterList.degQuarter6);
                    this.degQuarterList.degQuarter6 = parseInt(this.degQuarterList.degQuarter6) - parseInt(this.degQuarterList.degQuarter5);
                    this.degQuarterList.degQuarter5 = parseInt(this.degQuarterList.degQuarter5) - parseInt(this.degQuarterList.degQuarter4);
                    this.degQuarterList.degQuarter4 = parseInt(this.degQuarterList.degQuarter4) - parseInt(this.degQuarterList.degQuarter3);
                    this.degQuarterList.degQuarter3 = parseInt(this.degQuarterList.degQuarter3) - parseInt(this.degQuarterList.degQuarter2);
                    this.degQuarterList.degQuarter2 = parseInt(this.degQuarterList.degQuarter2) - parseInt(this.degQuarterList.degQuarter1);
                    this.degQuarterList.degQuarter1 = parseInt(this.degQuarterList.degQuarter1) + 25;
                    this.$emit('getInputContentText',[this.textQuarterList.textQuarter1, this.textQuarterList.textQuarter2, this.textQuarterList.textQuarter3,this.textQuarterList.textQuarter4,this.textQuarterList.textQuarter5,this.textQuarterList.textQuarter6,this.textQuarterList.textQuarter7,this.textQuarterList.textQuarter8])
                }
            },
            sum: function(){
                let summe = parseInt(this.degQuarterList.degQuarter1)+parseInt(this.degQuarterList.degQuarter2)+parseInt(this.degQuarterList.degQuarter3)+parseInt(this.degQuarterList.degQuarter4)+parseInt(this.degQuarterList.degQuarter5)+parseInt(this.degQuarterList.degQuarter6)+parseInt(this.degQuarterList.degQuarter7)+parseInt(this.degQuarterList.degQuarter8);
                return summe;
            },
        }
    }
</script>

<style scoped>
    .w-max {
        max-width: 45px;
    }
</style>