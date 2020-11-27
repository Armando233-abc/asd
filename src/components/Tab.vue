<template>
    <div class="tab">
        <span class="emoji">{{emoji}}</span>
        <span class="testo">{{testo}}</span>
    </div>
</template>

<script>
export default {
    name : "Tab",
    props : {
        testo : String,
        emoji : String
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Fondamento&display=swap%27');

    div{
       display: grid; 
       grid-template-rows: 5fr 3fr;
       place-items: center;
    }
    
    .emoji{
        font-size: 26px;
    }

    .testo{
        font-family: 'Fondamento', cursive;
    }
</style>