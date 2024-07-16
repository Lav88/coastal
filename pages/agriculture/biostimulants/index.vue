<template>
    <div class="">
        
        <!-- BOX A -->
        <section class="box box-a bg-primary text-center py-md">
            <div class="Project-sectionInner">
                <span class="Project-label Project-label--floating">Carbon footprint</span> 
                <h2 class="Project-title h2">-316 <small>TonCO₂eq</small></h2> 
                <p class="text-md">Lorem, ipsum dolor sit am inventore ex autem officiis voluptates quisquam!
                    <a href="">Learn More</a>
                </p>
            </div>
        </section>


      
            
            <ProductPreview
            id="allPurpose"
            thumbnail="~static/img/biostimulants/cereals-product.png"
            title="All purpose"
            previewText="lorem osomef ejhrzg ehfedhfg efe wewr "/>

            <ProductPreview
            id="allPurpose"
            thumbnail="/img/biostimulants/product-example"
            title="All purpose"
            previewText="lorem osomef ejhrzg ehfedhfg efe wewr "/>

            <ProductPreview
            id="allPurpose"
            thumbnail="/img/biostimulants/product-example"
            title="All purpose"
            previewText="lorem osomef ejhrzg ehfedhfg efe wewr "/>
           

        <section class="box box-c bg-primary grid-col-2 grid-reversed">
            
        </section>
 
        

    </div>
</template>
<script>
import ProductPreview from '@/components/Products/ProductPreview'
export default {
    components: {
        ProductPreview
    },
    data() {
        return {
            userId: ''
        }
    },
    methods: {
        onLoadUser() {
            this.$router.push('/agriculture/biostimulants/' + this.userId)
        }
    }
}

</script>
<style scoped>


</style>