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
    width: auto;
    display: flex;
    flex-direction: column;
    border: 1px solid #004aad;
    margin-top: 5px;
    background-color: red;
    align-items: center;
    justify-content: center;
}

.acoes button {
    width: 50px;
    height: 50px;
    border: 1px solid #004aad;
    background: white;
    padding: 10px;
}

.acoes button:hover {
    width: 50px;
    height: 50px;
    border: 1px solid white;
    background: #004aad;
    color: white;
    padding: 10px;
}
</style>