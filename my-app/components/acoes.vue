<template>
        <section class="acoes">
            <button @click="$emit('somar')">+</button>
            <button @click="$emit('subtrair')">-</button>
            <button @click="$emit('igual')">=</button>
            <button @click="$emit('limpar')">C</button>
        </section>
</template>

<style>
.acoes {
    background-color: cadetblue;
    padding: 10px;
    width: auto;
    display: flex;
    flex-direction: column;
}

.acoes button {
    width: 50px;
    height: 50px;
    border: 1px solid #004aad;
    font-size: 16px;
}
</style>