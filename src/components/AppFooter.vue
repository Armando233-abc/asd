<!--Ogni programma di vue prevede 4 tag-->

<template>
    <footer>
        <tab emoji="🎅" testo="Estrazione" />
        <tab emoji="🎄" testo="Cartellone" />
        <tab emoji="⚙" testo="Impostazioni" />
        <tab emoji="" testo="tabellone"></tab>
    </footer>
</template>

<script>
import Tab from './Tab'
export default{
    name : "AppFooter",
    components: { Tab },

        Tab}
</script>


<style>
    footer{
        background: var(--bianco);
        height: 80px;
        position: fixed;
        width: 100vw;
        bottom: 0;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }

</style>