<template>
    <table class="table table-hover">
        <thead>
        <tr class="bg-dark text-white">
            <th scope="col">Sprache</th>
            <th scope="col">Selbsteinschätzung</th>
            <th scope="col">Erfahrung in Jahren</th>
            <th scope="col">Woher kommt die Erfahrung</th>
        </tr>
        </thead>
        <tbody>
        <p-languages-tabline v-for="(List, index) in skillsList" :key="index" :skills="List"></p-languages-tabline>
        </tbody>
    </table>
</template>

<script>
    import PLanguagesTabline from "./p-languages-tabline";
    export default {
        name: "p-languages",
        components: {PLanguagesTabline},
        data() {
            return {
                skillsList: [
                    {id:0, name: "HTML / CSS", selfRating: "Experte", years:"19", fount:"Schulfach, Umschulungsfach, Selbststudium"},
                    {id:1, name: "SASS", selfRating: "Fortgeschritten", years:"0,5", fount:"Selbststudium"},
                    {id:1, name: "PHP", selfRating: "Fortgeschritten", years:"4", fount:"Umschulungsfach, Selbststudium"},
                    {id:1, name: "Java", selfRating: "Grundkenntnisse", years:"0,5", fount:"Studienfach"},
                    {id:1, name: "C+", selfRating: "Grundkenntnisse", years:"0,5", fount:"Studienfach"},
                    {id:1, name: "C#", selfRating: "Grundkenntnisse", years:"0,5", fount:"Umschulungsfach, Selbststudium"},
                ]
            }
        }
    }
</script>

<style scoped>

</style>