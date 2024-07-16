<template>
    <div class="LayoutTwo-text LayoutTwo-size30 Sustainability-text">
        <header class="Sustainability-title">
            <h2 class="h2">{{ leadText }}</h2>
        </header> 
        <div class="LayoutTwo-paragraphs Hiring-content">
            <p class="Paragraph">{{ textOne }}</p>
            <p class="Paragraph">{{ textTwo }}</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ThreeSection',
    props: {
        leadText: {
            type: String,
            required: true
        },
        textOne: {
            type: String
        },
        textTwo: {
            type: String
        }
    }
}
</script>