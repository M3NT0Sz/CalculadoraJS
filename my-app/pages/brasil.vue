<template>
    <ul v-for="brasil in this.brasil">
        <li>Nome Comum: {{ this.brasil[0].name.common }} </li>
        <li>Nome Oficial: {{ this.brasil[0].name.official }} </li>
        <li>Nome Moeda: {{ this.brasil[0].currencies.BRL.name }} </li>
        <li>Simbolo Moeda: {{ this.brasil[0].currencies.BRL.symbol }} </li>
        <li>Capital: {{ brasil.capital }} </li>
        <li>Região: {{ brasil.region }} </li>
        <li>SubRegião: {{ brasil.subregion }} </li>
        <li>Fronteiras: {{ brasil.borders }} </li>
    </ul>
</template>
<script>
    import brasil from "../brasil.json"

    export default {
    data() {
        return {
            brasil: brasil,
            nomeC: "",
            nomeO: "",
            nomeM: "",
            simboloM: "",
            serie: "",
            cont: 0
        }
    }
}
</script>