<template>
    <div class="page-container">
        <section position="relative">
            <div class="custom-shape-divider-top-1632854930">
                <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                    <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill"></path>
                    <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill"></path>
                    <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill"></path>
                </svg>
            </div>
        </section>
        <div class="ca-container">
            <div class="a-container mx-auto">
                    <div class="mx-auto title-container mt-10 mb-15 pa-10 noir-text">
                        &lt;About Me&gt;
                    </div>
                    <p class="noir-text">
                        My name is Mohammed Al-Shaibani, I am a fourth year computer science student at the University
                        of Windsor. I am a software developer with albinism. My main goal is to use the increasing 
                        advance of modern software and technologies to help those with low vision live a more accessible life.
                    </p>
            </div>
            <div class="c-container mx-auto">
                    <div class="mx-auto title-container mt-10 mb-15 pa-10 noir-text">
                        &lt;Contact Me&gt;
                    </div>
                    <v-btn @click="btnClick('https://github.com/MohammedShaibani')" class="btn-align" width="115" color="white" plain>
                    <v-icon left color="rgb(21, 22, 24)" size="30">mdi-github</v-icon>
                    Github
                    </v-btn>
                    <v-btn @click="btnClick('https://www.linkedin.com/in/moea/')" class="btn-align" width="115" color="white" plain>
                    <v-icon left color="rgb(21, 22, 24)" size="30">mdi-linkedin</v-icon>
                    LinkedIn
                    </v-btn>
                    <v-btn @click="btnClick('mailto:therealmoe9@gmail.com?subject=Lets%20Connect')" class="btn-align" width="115" color="white" plain>
                    <v-icon left color="rgb(21, 22, 24)" size="30">mdi-gmail</v-icon>
                    Email
                    </v-btn>
            </div>
        </div>
        <slot name="btn"></slot>
    </div>
</template>

<script>
export default {
    methods: {
        btnClick: function(link) {
            window.open(link);
        }
    }

}
</script>

<style scoped>
.page-container {
    background-color: #41B883;
    display: flex;
    flex-direction: column;
}
.ca-container {
    padding: 20px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
}
.a-container {
    margin: 20px;
    display: flex;
    width: 340px;
    height: 500px;
    flex-direction: column;
    justify-content: flex-start;
    align-content: flex-start;
    align-items: flex-start;
    text-align: center;
}
.c-container {
    margin: 20px;
    width: 370px;
    height: 500px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    align-content: center;
    text-align: center;
}
.title-container {
    display: flex;
    flex-direction: column;
    align-content: flex-start;
    justify-content: center;
    text-align: center;
    font-size: 40px;
}
.btn-align {
    justify-content: start;
}
.noir-text {
    font-family: 'Noir-regular';
    color: white;
}
.custom-shape-divider-top-1632854930 {
    position: relative;
    top: 0;
    left: 0;
    width: 100vw;
    overflow: hidden;
    line-height: 0;
}

.custom-shape-divider-top-1632854930 svg {
    position: relative;
    display: block;
    width: calc(177% + 1.3px);
    height: 37px;
}

.custom-shape-divider-top-1632854930 .shape-fill {
    fill: #151618;
}
</style>