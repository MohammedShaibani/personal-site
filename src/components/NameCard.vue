<template>
    <v-card
    class=" mx-auto my-auto flexbox-container"
    max-width="750"
    color="rgb(255, 0, 0, 0)"
    elevation="0"
  >
    <v-img 
        :src="require('../assets/site-avatar.jpg')" 

        max-height="100"
        max-width="100"
        class ='rounded-circle flex-item-img'
    ></v-img>

    <v-card-text class="text--primary mx-auto">
        <div id="myname" class=" mt-2 mx-auto flex-item-text text-center font-size-title font-family">Hi, my name is Mohammed</div>
        <div id="developer" class="mx-7 flex-item-text text-center font-size-subtitle font-family">&lt;Software Developer&gt;</div>
        <div id="student" class="mx-14 flex-item-text text-center font-size-subtitle font-family">&lt;/Student&gt;</div>
    </v-card-text>

  </v-card>
</template>

<script>
export default {
    methods: {
        scrollDown() {
            console.log("Scroll Emitter");
            this.$emit("scrollDown");
        }
  }
}
</script>

<style scoped>
.flexbox-container {
    display: flex;
    align-content: flex-start;
    justify-content: center;
    background-color: rgb(21, 22, 24);
    flex-wrap: wrap;
    height: 80vh;
}
.flex-item-img {
    display: flex-start;
    margin: 1px;
    flex-wrap: wrap;
}
.flex-item-text {
    display: flex-start;
    flex-direction: column;
    justify-content: center;
    flex-wrap: wrap;
}
.font-size-title {
    font-size: 40px;
    line-height: 1.2;
}
.font-size-subtitle {
    font-size: 20px;
}
.bolded {
    font-weight: bold;
}
.font-family {
    font-family: 'Noir-regular';
    font-weight: bold;
}

</style>