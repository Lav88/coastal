<template>
    <section class="Cost LayoutTwo-vertical section fp-noscroll fp-auto-height-responsive fp-section fp-table" data-tooltip="Benefits" data-anchor="Benefits" data-fp-styles="null" style="height: 730px;">
        <div class="fp-tableCell" style="height: 730px;">
            <div class="LayoutTwo-media LayoutTwo-size70">
                <div class="LayoutTwo-mobileMask LayoutTwo-mobileMask--fromLeft u-mediaZoomAnimation LayoutTwo-mobileMask--full">
                    <img :src="landing"
                    class="u-mediaFullSize"> <!---->
                </div> 
                <ul class="Stats Cost-stats">
                    <li class="Stats-item Cost-statsItem"><span><strong>{{ dataPoints }}</strong> faster</span></li>
                    <li class="Stats-item Cost-statsItem"><span><strong>+10%</strong> added square</span></li>
                    <li class="Stats-item Cost-statsItem"><span><strong>-50% </strong>less materials used</span></li>
                </ul>
            </div> 
            <div class="LayoutTwo-text LayoutTwo-split LayoutTwo-size30 Cost-text">
                <header>
                    <h2 class="h2">{{ title }} </h2>
                </header> 
                <div class="LayoutTwo-paragraphs">
                    <h4>{{ previewText  }} </h4>
            
                    <p><br>{{ displayText }}</p>

                    <p><a href="mailto:hello@lekolabs.com">{{ btnLinkText }}</a></p>
                </div>
                
            </div>
        </div>
    </section> <!----> 
</template>
<script>
export default {
    name: 'DataImgPreview',
    props: {
        title: {
            type: String,
            required: true
        },
        previewText: {
            type: String,
            required: true,
        },
        displayText: {
            type: String,
            required: true,
        },
        btnLinkText: {
            type: String,
            required: true
        },
        pictureSrc: String,
        dataPoints: {
            type: String,
            required: true
        }
    }
}
</script>