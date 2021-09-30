<template>
<div class="s-bubble-container mb-2">
      <div>
        <div @mouseover="active=true" @mouseleave="active=false" class="icon-container mx-3 mt-2">
            <slot></slot>
        </div>
        <div class="s-name-container noir-font" v-show="active">
            {{langName}}
        </div>
  </div>
</div>

</template>

<script>
export default {
    data: function () {
        return {
            active: false
        }
    },
    props: [
        'langName'
    ]
}
</script>

<style>
.s-bubble-container {
    display: flex;
    flex-direction: column;;
    height: 10vh;
}
.icon-container {
    height: 50px;
    width: 50px;
    background-color: rgb(21, 22, 24);
    border-radius: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
}
.s-name-container {
    color: rgb(21, 22, 24);
    justify-content: center;
    text-align: center;
}
.noir-font {
    font-family: 'Noir-regular';
}
.s-bubble-container:hover {
    transform: scale(1.2);
    transition: all 0.3s ease;
}
.icon-container:hover {
    background-color: #41B883;
}
</style>