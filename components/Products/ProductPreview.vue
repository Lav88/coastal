<template>
    <div class="box box-d bg-secondary grid-col-2">
        <div 
        class="productPreview-img"
        :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
        <img src="" alt="">
            <div class="box-text">
                <h2 class="text-xl">{{ title }}</h2>
                <p class="text-md">{{ previewText }}</p>
                <nuxt-link :to="'/agriculture/biostimulants/' + id">See more</nuxt-link>
            </div>
    </div>
</template>
<script>
export default {
    name: 'ProductPreview',
    props: {
        id: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        previewText: {
            type: String,
            required: true
        },
        thumbnail: {
            type: String,
            required: true
        }
    }
}
</script>
<style scoped>
/* TEXT STYLING*/
.text-center {
    text-align: center;
}

.text-sm {
    font-size: 19px;
    margin-bottom: 20px;
}

.text-md {
    font-size: 24px;
    margin-bottom: 20px;
}

.text-lg {
    font-size: 40px;
    text-transform: uppercase;
    margin-bottom: 20px;
}

.text-xl {
    font-size: 50px;
    text-transform: uppercase;
    letter-spacing: 6px;
    font-weight: 600;
    margin-bottom: 20px;
}

@media(max-width: 960px) {
    .text-xl {
        font-size: 30px
    }
    .text-lg {
        font-size: 20px;
    }
    .text-md {
        font-size: 19px;
    }
}

:root {
    --colour-flowers: #e1ac44;
    --colour-scondary: #0b2819;
    --colour-extra-red: #d4e9e2;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html, body {
    line-height: 1.4;
    color: #111;
}

a {
    color: #111;
}

ul {
    list-style: none;
}

p {
    margin: 5px 0;
    line-height: 1.7;
}

.productPreview-img {
    max-width: 100%;
}

section a {
    color: white;
}

/* BACKGROUNDS*/
.bg-primary {
    background-color: #0b2819 !important;
    color: #fff;
}

.bg-secondary {
    background-color: #f4f4f4 !important;
    color: #111;
}

.bg-extra {
    background-color: rgb(117, 8, 8) !important;
    color: #fff;
}

.bg-dark {
    background-color: #111;
    color: #111;
}



@media (max-width: 768px) {
    .grid-col-2 {
        grid-template-columns: 1fr;
    }
    .grid-reversed :first-child {
        order: 0;
    }
}

@media (min-width: 1440px) {
    .box {
        max-width: 1440px;
        margin-right: auto;
        margin-left: auto;
    }
}

.box {
    margin-bottom: 30px;

}

.box-inner {
    max-width: 700px;
    margin: 0 auto;
}

.box-text {
    max-width: 500px;
    text-align: center;
    justify-self: center;
    padding: 20px 0;
    margin: 0 auto;
}

.box-text .btn {
    margin-top: 20px;
}

.box-f .box-text {
    max-width: 600px;;
}
/*grid-styles*/
.grid-col-2 {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
    align-items: center;
    justify-content: space-between;
}

.grid-reversed :first-child {
    order:2;
}

/* Padding */
.py-sm {
    padding: 10px 0;
}

.py-md {
    padding: 20px 0;
}

.py-lg {
    padding: 40px 0;
}


</style>