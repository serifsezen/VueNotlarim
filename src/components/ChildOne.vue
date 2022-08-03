<template>
    <div>
        <h1>cihild one componenet</h1>
        <p>Kullanici Adi:{{name}}</p>
        <button @click="sendToParent">Veriyi parente gonder</button>
    </div>
</template>

<script>
export default {
    props:["name"],
    setup() {
    },
    methods:{
        sendToParent(){
            this.$emit("data","veri gelidiiii")
        }
    }
}
</script>