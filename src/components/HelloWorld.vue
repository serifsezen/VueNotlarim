<template>
    <div class="helloclass">
        <h1>Burasi HelloWorld</h1>
         <form class="form" @submit.prevent="dersEkle">
            <!-- prevent sayfayý tekrardan yüklemeden ekleme iþlemini gerçekleþtirir  -->
            <input type="text" placeholder="Ders Ekle" v-model="dersler"/>
        </form>
        <ul>
            <li v-for="(veri,index) in veriler" :key="index">{{index+1}} {{veri.ders}}</li>
        </ul>
        <p v-if="veriler.length>0"> Ders sayisi: {{veriler.length}}</p>
        <p v-else>Dersler eklenmemis</p>
    </div>
</template>


<script>
export default {
    data(){
        return{
            dersler:"",
            veriler:[
                // {"ders":"Matematik"},
                // {"ders":"Fizik"},
            ]
        }
    },
    methods:{
        dersEkle(){
            this.veriler.push({ders:this.dersler})
            this.dersler='';
        }
    }
}
</script>

<style>
.helloclass{
    background-color: rgb(236, 228, 228);
}
ul{
    list-style-type: none;
}
ul li{
    padding: 5px;
    background-color:rgb(228, 222, 222);
    border-left: 5px solid;
    border-right: 5px solid;
    margin-bottom: 2px;
    margin-right: 30px;
}
p{
    text-align: center;
    padding: 5px;
}
h1{
    padding: 5px;
    text-align: center;
}
.form{
    text-align: center;
}
input{
    
    border: 0;
    padding: 5px;
    box-shadow: 0px 0px 12px #888;
}
</style>