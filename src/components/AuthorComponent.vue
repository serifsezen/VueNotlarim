<template>
    <div>
        <h1>Author Componenti</h1>
        <button @click="arttir">Arttir</button>
        <p>{{sayac}}</p>
    </div>
</template>

<script>
export default {
    setup() {
        
    },
    data(){
        return{
            sayac:0
        }
        
    },
    methods:{
        arttir(){
            this.sayac++
        }
    }
}
</script>