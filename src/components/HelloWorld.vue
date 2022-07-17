<template>
    <div>
        <h1>Burasi HelloWorld</h1>
        <ul>
            <li v-for="(veri,index) in veriler" :key="index">{{index}} {{veri.ders}}</li>
        </ul>
        <p v-if="veriler.length>0"> Ders sayisi: {{veriler.length}}</p>
        <p v-else>Dersler eklenmemis</p>
    </div>
</template>


<script>
export default {
    data(){
        return{
            veriler:[
                {"ders":"Matematik"},
                {"ders":"Fizik"},
            ]
        }
    }
}
</script>

<style>

</style>