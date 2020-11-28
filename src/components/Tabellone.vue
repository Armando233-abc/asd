<template>
    <div>
        <h1>{{ isNaN(estratto)? '-': estratto}}</h1>
        <h2>{{ voce === ""? "-" : voce["napoletano"]}}</h2>
        <h3>{{ voce === ""? "-" : voce["italiano"]}}</h3>
        <div>{{lista_estratti.length}}</div>
        <button @click="estrai()">Estrai</button>
        <ul>
            <li v-for="(numero, indice) in lista_estratti" :key="indice">{{numero}}</li>
        </ul>
    </div>
    
</template>


<script>
import Smorfia from '../dependences/tombola-api/smorfia.json'

export default {
    name: "Tabellone",
    data(){
        return {
            estratto : NaN, //Not a Number
            voce : "",
            lista_estratti : []
        }
    },
    methods : {
        estrai(){
            if (this.lista_estratti.length < 90){
                let numero = Math.floor(Math.random() * 90 + 1)
                while (this.lista_estratti.includes(numero)){
                    numero = Math.floor(Math.random() * 90 + 1)
                }
                this.estratto = numero
                this.voce = Smorfia[numero.toString()]
                this.lista_estratti.push(numero)
                let italiano = Smorfia[numero.toString()]["italiano"]
                let frase = new SpeechSynthesisUtterance(italiano)
                speechSynthesis.speak(frase)
            }
        }
    }
}
</script>

<style>

</style>