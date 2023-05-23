<script>


export default {
    components: {
       
    },
    data() {
        return {
          
    }},
    props: [
        "searchResultcode",
        "selleraccount",
        "date",
        "description",
        "name",
        "number",
        "place",
        "price",
        "type",
        
    ],
    methods: {
        push() {
        //  console.log(this.searchResultcode);
         this.$emit("emitPush",this.searchResultcode)
        },
        
        
        
    },
    // 生命週期}
    mounted() {
        // this.fn();


    }
}




</script>


<template>
<div class="card">
<div class="explainAndBtn">
    <img src="../assets/img/sweet-potato-600x400.jpg" alt="">
     <div class="explain">
        <p>編號: {{ searchResultcode }}</p>
        <p>產品分類: {{type}} </p>
        <p>產品敘述: {{description}} </p>
        <p>產品名稱: {{name}} </p>
        <p>產品數量: {{number}} </p>
        <p>產品價格: {{price}} </p>
        <p>生產日期: {{date}} </p>
        <p>生產產地: {{place}} </p>
        
       
     </div>

    <button type="button" class="addCartBTN" @click="push">
    <i class="fa-solid fa-basket-shopping">加入購物車</i>
    </button>
</div>
</div>


  
</template>


<style lang="scss" scoped>
.card{
overflow-y: auto;
flex-direction: column;
display: flex;
justify-content: center;
align-items: center;
background-repeat: no-repeat;
background-size:cover;
margin: 10px;
border-radius: 5px;
width: 20vw;
height: 30vh;
background: #ffffff;
border:2px solid #454141;

img{
    border-radius: 5px;
    width: 180px;
    height: 120px;
}
}
.explainAndBtn{
    margin-top:230px ;
    flex-direction: column;
    display: flex;
    justify-content: center;
    align-items: center;
}
.explain{
    flex-direction: column;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin:0 5px ;
}
.addCartBTN{
    border-radius: 20px;
    background: #454141;
    color: antiquewhite;
    transition: 1s;
}
.addCartBTN:hover{
    background:antiquewhite;
    color: #454141;
    scale: 1.1;
}
.addCartBTN:active{
    scale: 0.9;
}
</style>
