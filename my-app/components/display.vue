<template>
    <section class="resultado">
        {{ valor }}
    </section>
</template>

<script>

export default{

    props: {
        valor:{
            required: true
        }
    }

}

</script>

<style>
.resultado {
    padding-right: 5px;
    text-align: right;
    font-size: 40px;
    margin: 5px;
    width: auto;
    height: 50px;
    border: 1px solid #004aad;
    background-color: blueviolet;
}
</style>