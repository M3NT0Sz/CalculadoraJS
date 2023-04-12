<template>
    <form @submit.prevent="$e => salvarAluno()">
        <input type="text" placeholder="Nome" v-model="nome">
        <input type="number" min="0" max="100" placeholder="Idade" v-model="idade">
        <input type="text" placeholder="Série" v-model="serie">
        <button type="submit">Salvar</button>
    </form>
    <hr>
    <ul v-for="(aluno,index) in this.dados">
            <li>Codigo: {{ index }} </li>
            <li>Nome: {{ aluno.nome }} </li>
            <li>Idade: {{ aluno.idade }} </li>
            <li>Série: {{ aluno.serie }} </li>
            <button @click="$e => apagarAluno(index)">Deletar</button>
    </ul>
</template>

<script>
import dados from "../alunos.json"

export default {
    data() {
        return {
            dados: dados,
            nome: "",
            idade: "",
            serie: "",
            cont: 0
        }
    },
    methods: {
        salvarAluno() {
            this.nome
            this.idade
            this.serie
            this.dados.push({ "nome": this.nome, "idade": this.idade, "serie": this.serie })
        },
        apagarAluno(index) {
            this.dados.splice(index, 1);
        }
    }
}
</script>