<template>
    <div>
        <h1>Burasi HelloWorld</h1>
        <ul>
            <li v-for="(veri,index) in veriler" :key="index">{{index}} {{veri.ders}}</li>
        </ul>
        
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