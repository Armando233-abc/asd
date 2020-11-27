<!--Ogni programma di vue prevede 4 tag-->

<template>
    <footer>
        <tab emoji="🎅" testo="Cartellone" />
        <tab emoji="🎄" testo="Cartella Singola" />
        <tab emoji="⚙" testo="Impostazioni" />
    </footer>
</template>

<script>
import Tab from './Tab'
export default{
    name : "AppFooter",
    components: { Tab },
}
</script>


<style>
    footer{
        background: var(--bianco);
        height: 80px;
        position: fixed;
        width: 100vw;
        bottom: 0;
        display: grid;
        grid-template-columns: 1fr 2fr 1fr;
    }

</style>