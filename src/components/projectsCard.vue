<template>
  <div class="card mx-5 my-5">     
        <div class="card-img mx-auto">
            <v-img
            class="v-img-border"
            :src="require(`../assets/${image}`)"
            ></v-img>
        </div>
        <div class="card-title mx-auto font-family" @click="btnClick(url)">{{title}}</div>
        <div class="card-text font-family">{{text}}</div>
  </div>
</template>

<script>
export default {
    props: ['id','image','title','url','text'],
    methods: {
        btnClick (link) {
            window.open(link);
        }
    }

}
</script>

<style scoped>
.card {
    justify-content: center;
    align-content: center;
    background-color: white;
    min-width: 200px;
    max-width: 260px;
    min-height: 400px;
    border-radius: 18px;
}
.card-img {
    height: 145px;
    background-size: cover;
    border-radius: 15px 15px 0 0;
}
.v-img-border {
    border-radius: 15px 15px 0 0;
}
.card-title {
    text-align: center;
    background-color: rgb(21, 22, 24);
    color: white;
    padding: 5px 0 5px 0;
    font-size: 30px;
}
.card-text {
    text-align: center;
    color: black;
    margin: auto;
    padding: 6px;
}
.font-family {
    font-family: 'Noir-regular';
}
.card:hover {
    background-color: white;
    transform: scale(1.05);
    transition: all 0.3s ease;
    outline: none;
    border: none;
}
.card-title:hover {
    cursor: pointer;
    background-color: #41B883;
}
</style>