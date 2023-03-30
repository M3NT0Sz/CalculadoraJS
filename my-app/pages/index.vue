<template>
    <body>
        <main>
            <Display :valor="display" />
            <section class="arrumar">
                <Numeros @digitar="digitar" />
                <Acoes @limpar="limpar" @somar="somar" @subtrair="subtrair" @igual="igual" />
            </section>
        </main>
    </body>
</template>

<script>

export default {
    data() {
        return {
            display: "",
            n1: "",
            n2: "",
            operacao: ""
        }
    },

    methods: {
        digitar(valor) {
            if(this.calculo === "conta"){
                this.limpar()
                this.calculo = ""
            }
            this.display = this.display + valor
        },
        somar() {
            this.n1 = parseInt(this.display),
                this.display = "",
                this.calculo = "somar"
        },
        subtrair() {
            this.n1 = parseInt(this.display),
                this.display = "",
                this.calculo = "subtrair"
        },
        igual() {
            if(this.calculo === "somar"){
                this.n2 = parseInt(this.display),
                this.display = this.n1 + this.n2
                this.calculo = "conta"
            } else {
                this.n2 = parseInt(this.display),
                this.display = this.n1 - this.n2
                this.calculo = "conta"
            }
        },
        limpar() {
            this.display = ""
            this.n1 = ""
            this.n2 = ""
        }
    }
}

</script>

<style scoped>
body {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
}

main {
    display: block;
    margin: auto;
    background-color: aqua;
}

.arrumar {
    display: flex;
    flex-direction: row;
}
</style>