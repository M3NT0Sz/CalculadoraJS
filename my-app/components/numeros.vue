<template>
        <section class="botoes">
            <div class="num">
                <button @click="($e) => $emit('digitar', 1)">1</button>
                <button @click="($e) => $emit('digitar', 2)">2</button>
                <button @click="($e) => $emit('digitar', 3)">3</button>
            </div>
            <div class="num">
                <button @click="($e) => $emit('digitar', 4)">4</button>
                <button @click="($e) => $emit('digitar', 5)">5</button>
                <button @click="($e) => $emit('digitar', 6)">6</button>
            </div>
            <div class="num">
                <button @click="($e) => $emit('digitar', 7)">7</button>
                <button @click="($e) => $emit('digitar', 8)">8</button>
                <button @click="($e) => $emit('digitar', 9)">9</button>
            </div>
            <div class="num">
                <button @click="($e) => $emit('digitar', 0)">0</button>
            </div>
        </section>
</template>



<style>
.botoes {
    width: auto;
    display: flex;
    flex-direction: column;
    border: 1px solid #004aad;
    margin-top: 5px;
    background-color: red;
    align-items: center;
    justify-content: center;
}

.botoes button {
    width: 50px;
    height: 50px;
    border: 1px solid #004aad;
    background: white;
    padding: 10px;
}

.botoes button:hover {
    width: 50px;
    height: 50px;
    border: 1px solid white;
    background: #004aad;
    color: white;
    padding: 10px;
}

.num {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
}
</style>