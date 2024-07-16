<template>
    <body>
        
        <div class="App">
    
            <TheHeader @sidenavToggle="displaySidenav = !displaySidenav"/>
            <TheSidenav 
            :show="displaySidenav"
            @close="displaySidenav = false"/>
            <nuxt />
            <Footer />
        </div>
    </body>
</template>
<style>


</style>

<script>
import TheHeader from '~/components/Navigation/TheHeader.vue';
import TheSidenav from '~/components/Navigation/TheSidenav.vue';
import Footer from '~/components/Footer.vue';


export default {
  components: {
    TheHeader,
    TheSidenav,
    Footer
    },
    data() {
        return {
            displaySidenav: false
        }
    }
}
</script>
<style>


    a,abbr,acronym,address,applet,article,aside,audio,b,big,blockquote,body,canvas,caption,center,cite,code,dd,del,details,dfn,div,dl,dt,em,embed,fieldset,figcaption,figure,footer,form,h1,h2,h3,h4,h5,h6,header,hgroup,html,i,iframe,img,ins,kbd,label,legend,li,mark,menu,nav,object,ol,output,p,pre,q,ruby,s,samp,section,small,span,strike,strong,sub,summary,sup,table,tbody,td,tfoot,th,thead,time,tr,tt,u,ul,var,video {
        border: 0;
        font-size: 100%;
        font: inherit;
        margin: 0;
        padding: 0;
        vertical-align: baseline
    }

    article,aside,details,figcaption,figure,footer,header,hgroup,img,menu,nav,section {
        display: block
    }


    ol,ul {
        list-style: none
    }

    blockquote,q {
        quotes: none
    }

    blockquote:after,blockquote:before,q:after,q:before {
        content: "";
        content: none
    }

    table {
        border-collapse: collapse;
        border-spacing: 0
    }

    html {
        box-sizing: border-box
    }

    *,:after,:before {
        box-sizing: inherit
    }

    button,input,select {
        -webkit-appearance: none;
        -moz-appearance: none;
        border: 0;
        border-radius: 0;
        border-radius: initial;
        padding: 0
    }

    select {
        background: transparent none repeat 0 0/auto auto padding-box border-box scroll;
        background: initial;
        border-radius: 0;
        border-radius: initial;
        cursor: pointer
    }

    :focus {
        outline: 0
    }

    [type=submit],button {
        cursor: pointer
    }

    a {
        color: currentColor;
        -webkit-text-decoration: none;
        text-decoration: none
    }

    [type=search]::-ms-clear,[type=search]::-ms-reveal {
        display: none;
        height: 0;
        width: 0
    }

    [type=search]::-webkit-search-cancel-button,[type=search]::-webkit-search-decoration,[type=search]::-webkit-search-results-button,[type=search]::-webkit-search-results-decoration {
        display: none
    }



    @keyframes form-loading {
        0% {
            transform: scaleX(0);
            transform-origin: left
        }

        30%,70% {
            transform: scaleX(1)
        }

        to {
            transform: scaleX(0);
            transform-origin: right
        }
    }

    @keyframes fade-in {
        0% {
            opacity: 0
        }

        to {
            opacity: 1
        }
    }

    @keyframes news-content {
        0% {
            transform: translateY(30px)
        }
    }

    .NewsHomeSidebar-wys h2,.NewsSidebar-wys h2,.h2 {
        font-size: 2.875rem;
        letter-spacing: -.02em;
        line-height: 1.1
    }

    @media(min-width: 577px)and (max-width:1440px) {
        .NewsHomeSidebar-wys h2,.NewsSidebar-wys h2,.h2 {
            font-size:2rem
        }
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-wys h2,.NewsSidebar-wys h2,.h2 {
            font-size:1.4375rem
        }
    }

    .NewsHomeSidebar-wys h3,.NewsSidebar-blockquoteContent,.NewsSidebar-wys h3,.h3 {
        font-size: 2rem;
        line-height: 1.2
    }

    @media(min-width: 577px)and (max-width:1440px) {
        .NewsHomeSidebar-wys h3,.NewsSidebar-blockquoteContent,.NewsSidebar-wys h3,.h3 {
            font-size:1.625rem
        }
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-wys h3,.NewsSidebar-blockquoteContent,.NewsSidebar-wys h3,.h3 {
            font-size:1.25rem
        }
    }

    .NewsHomeSidebar-wys h4,.NewsHomeSidebar-wys p,.NewsSidebar-wys h4,.h4 {
        font-size: 1.625rem;
        letter-spacing: -.02em;
        line-height: 1.4
    }

    @media(min-width: 577px)and (max-width:1440px) {
        .NewsHomeSidebar-wys h4,.NewsHomeSidebar-wys p,.NewsSidebar-wys h4,.h4 {
            font-size:1.125rem;
            letter-spacing: -.005em
        }
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-wys h4,.NewsHomeSidebar-wys p,.NewsSidebar-wys h4,.h4 {
            font-size:.9375rem
        }
    }

    .NewsHomeSidebar-wys h5,.NewsSidebar-wys h5,.h5 {
        font-weight: 300
    }

    .Jobs-filterCurrent,.LayoutTwo-paragraphs li,.LayoutTwo-paragraphs p,.List,.NewsHomeSidebar-wys h5,.NewsSidebar-wys h5,.Paragraph,.h5 {
        font-size: .9375rem;
        letter-spacing: -.0066666667em;
        line-height: 1.5
    }

    @media(max-width: 1440px) {
        .Jobs-filterCurrent,.LayoutTwo-paragraphs li,.LayoutTwo-paragraphs p,.List,.NewsHomeSidebar-wys h5,.NewsSidebar-wys h5,.Paragraph,.h5 {
            font-size:.8125rem
        }
    }

    .Jobs-filterCurrent strong,.LayoutTwo-paragraphs li strong,.LayoutTwo-paragraphs p strong,.List strong,.NewsHomeSidebar-wys h5 strong,.NewsSidebar-wys h5 strong,.Paragraph strong,.h5 strong {
        font-weight: 600
    }

    .Paragraph--smaller {
        font-size: .8125rem
    }

    .List li {
        padding-left: 14px;
        position: relative
    }

    .List li+li {
        margin-top: .3125rem
    }

    .List li:before {
        content: "• ";
        left: 0;
        position: absolute;
        top: 2px;
        transform: scale(1.5)
    }

    .Subhead {
        display: inline-block;
        font-size: .625rem;
        font-weight: 500;
        letter-spacing: .1em;
        text-transform: uppercase
    }

    .Subhead--bigger {
        font-size: .75rem
    }


    html {
        height: -webkit-fill-available
    }

    @media(min-width: 993px) {
        @-moz-document url-prefix() {
            html {
                scrollbar-width:none
            }
        }

        html::-webkit-scrollbar {
            display: none;
            scrollbar-width: none;
        }
    }

    .is-lazy {
        opacity: 0.5;
        transition: opacity .3s linear
    }

    .is-lazy.is-loaded {
        opacity: 1
    }

    .is-leaving:not(.custom-transition) .App {
        opacity: 1;
        transition: opacity .25s
    }

    .is-leaving:not(.custom-transition) .Menu:before {
        background-color: #111;
        bottom: 0;
        content: "";
        left: 0;
        opacity: 1;
        position: fixed;
        right: 0;
        top: 0;
        transition: opacity .25s;
        z-index: 10
    }

    body {
        color: #111;
        /*font-family: NeueHaasGrotesk,sans-serif;*/
        font-family: "Space Grotesk", sans-serif;
        font-size: .9375rem;
        font-weight: 200;
        min-height: 100vh;
        margin: 0;
    }

    @supports(hover: none) {
        body {
            min-height:-webkit-fill-available
        }
    }

    strong {
        font-weight: 300
    }

    .is-unclickable {
        pointer-events: none
    }

    .App {
        background-color: #fff;
        min-height: 100vh
    }

    @media(max-width: 767px) {
        .App--fixed {
            bottom:env(safe-area-inset-bottom);
            left: 0;
            min-height: 0;
            min-height: auto;
            overflow: auto;
            position: fixed;
            right: 0;
            top: 0
        }
    }

    .MainPadding {
        padding-left: 40px;
        padding-right: 40px
    }

    @media(max-width: 992px) {
        .MainPadding {
            padding-left:8.6vw;
            padding-right: 8.6vw
        }
    }


    .fullpage-wrapper {
        background: #fff
    }

    .fp-responsive .fullpage-wrapper,.fullpage-wrapper.is-fixed {
        transform: none!important
    }

    .section {
        overflow: hidden;
        position: relative;
        z-index: 1
    }

    .fp-auto-height .fp-slide,.fp-auto-height .fp-tableCell,.fp-auto-height.fp-section,.fp-responsive .fp-auto-height-responsive .fp-slide,.fp-responsive .fp-auto-height-responsive .fp-tableCell,.fp-responsive .fp-auto-height-responsive.fp-section {
        height: auto!important
    }

    .fp-scrollable {
        overflow: hidden;
        position: relative
    }

    .is-safari .fp-scrollable {
        height: auto!important;
        overflow: visible;
        overflow: initial
    }

    .fp-scroller {
        overflow: hidden
    }

    .iScrollIndicator {
        border: 0!important
    }

    @font-face {
        font-family: swiper-icons;
        font-style: normal;
        font-weight: 400;
        src: url("data:application/font-woff;charset=utf-8;base64, d09GRgABAAAAAAZgABAAAAAADAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABGRlRNAAAGRAAAABoAAAAci6qHkUdERUYAAAWgAAAAIwAAACQAYABXR1BPUwAABhQAAAAuAAAANuAY7+xHU1VCAAAFxAAAAFAAAABm2fPczU9TLzIAAAHcAAAASgAAAGBP9V5RY21hcAAAAkQAAACIAAABYt6F0cBjdnQgAAACzAAAAAQAAAAEABEBRGdhc3AAAAWYAAAACAAAAAj//wADZ2x5ZgAAAywAAADMAAAD2MHtryVoZWFkAAABbAAAADAAAAA2E2+eoWhoZWEAAAGcAAAAHwAAACQC9gDzaG10eAAAAigAAAAZAAAArgJkABFsb2NhAAAC0AAAAFoAAABaFQAUGG1heHAAAAG8AAAAHwAAACAAcABAbmFtZQAAA/gAAAE5AAACXvFdBwlwb3N0AAAFNAAAAGIAAACE5s74hXjaY2BkYGAAYpf5Hu/j+W2+MnAzMYDAzaX6QjD6/4//Bxj5GA8AuRwMYGkAPywL13jaY2BkYGA88P8Agx4j+/8fQDYfA1AEBWgDAIB2BOoAeNpjYGRgYNBh4GdgYgABEMnIABJzYNADCQAACWgAsQB42mNgYfzCOIGBlYGB0YcxjYGBwR1Kf2WQZGhhYGBiYGVmgAFGBiQQkOaawtDAoMBQxXjg/wEGPcYDDA4wNUA2CCgwsAAAO4EL6gAAeNpj2M0gyAACqxgGNWBkZ2D4/wMA+xkDdgAAAHjaY2BgYGaAYBkGRgYQiAHyGMF8FgYHIM3DwMHABGQrMOgyWDLEM1T9/w8UBfEMgLzE////P/5//f/V/xv+r4eaAAeMbAxwIUYmIMHEgKYAYjUcsDAwsLKxc3BycfPw8jEQA/gZBASFhEVExcQlJKWkZWTl5BUUlZRVVNXUNTQZBgMAAMR+E+gAEQFEAAAAKgAqACoANAA+AEgAUgBcAGYAcAB6AIQAjgCYAKIArAC2AMAAygDUAN4A6ADyAPwBBgEQARoBJAEuATgBQgFMAVYBYAFqAXQBfgGIAZIBnAGmAbIBzgHsAAB42u2NMQ6CUAyGW568x9AneYYgm4MJbhKFaExIOAVX8ApewSt4Bic4AfeAid3VOBixDxfPYEza5O+Xfi04YADggiUIULCuEJK8VhO4bSvpdnktHI5QCYtdi2sl8ZnXaHlqUrNKzdKcT8cjlq+rwZSvIVczNiezsfnP/uznmfPFBNODM2K7MTQ45YEAZqGP81AmGGcF3iPqOop0r1SPTaTbVkfUe4HXj97wYE+yNwWYxwWu4v1ugWHgo3S1XdZEVqWM7ET0cfnLGxWfkgR42o2PvWrDMBSFj/IHLaF0zKjRgdiVMwScNRAoWUoH78Y2icB/yIY09An6AH2Bdu/UB+yxopYshQiEvnvu0dURgDt8QeC8PDw7Fpji3fEA4z/PEJ6YOB5hKh4dj3EvXhxPqH/SKUY3rJ7srZ4FZnh1PMAtPhwP6fl2PMJMPDgeQ4rY8YT6Gzao0eAEA409DuggmTnFnOcSCiEiLMgxCiTI6Cq5DZUd3Qmp10vO0LaLTd2cjN4fOumlc7lUYbSQcZFkutRG7g6JKZKy0RmdLY680CDnEJ+UMkpFFe1RN7nxdVpXrC4aTtnaurOnYercZg2YVmLN/d/gczfEimrE/fs/bOuq29Zmn8tloORaXgZgGa78yO9/cnXm2BpaGvq25Dv9S4E9+5SIc9PqupJKhYFSSl47+Qcr1mYNAAAAeNptw0cKwkAAAMDZJA8Q7OUJvkLsPfZ6zFVERPy8qHh2YER+3i/BP83vIBLLySsoKimrqKqpa2hp6+jq6RsYGhmbmJqZSy0sraxtbO3sHRydnEMU4uR6yx7JJXveP7WrDycAAAAAAAH//wACeNpjYGRgYOABYhkgZgJCZgZNBkYGLQZtIJsFLMYAAAw3ALgAeNolizEKgDAQBCchRbC2sFER0YD6qVQiBCv/H9ezGI6Z5XBAw8CBK/m5iQQVauVbXLnOrMZv2oLdKFa8Pjuru2hJzGabmOSLzNMzvutpB3N42mNgZGBg4GKQYzBhYMxJLMlj4GBgAYow/P/PAJJhLM6sSoWKfWCAAwDAjgbRAAB42mNgYGBkAIIbCZo5IPrmUn0hGA0AO8EFTQAA") format("woff")
    }

    :root {
        --swiper-theme-color: #007aff
    }

    .swiper-container {
        list-style: none;
        margin-left: auto;
        margin-right: auto;
        overflow: hidden;
        padding: 0;
        position: relative;
        z-index: 1
    }

    .swiper-container-vertical>.swiper-wrapper {
        flex-direction: column
    }

    .swiper-wrapper {
        box-sizing: content-box;
        display: flex;
        height: 100%;
        position: relative;
        transition-property: transform;
        width: 100%;
        z-index: 1
    }

    .swiper-container-android .swiper-slide,.swiper-wrapper {
        transform: translateZ(0)
    }

    .swiper-container-multirow>.swiper-wrapper {
        flex-wrap: wrap
    }

    .swiper-container-multirow-column>.swiper-wrapper {
        flex-direction: column;
        flex-wrap: wrap
    }

    .swiper-container-free-mode>.swiper-wrapper {
        margin: 0 auto;
        transition-timing-function: ease-out
    }

    .swiper-slide {
        flex-shrink: 0;
        height: 100%;
        position: relative;
        transition-property: transform;
        width: 100%
    }

    .swiper-slide-invisible-blank {
        visibility: hidden
    }

    .swiper-container-autoheight,.swiper-container-autoheight .swiper-slide {
        height: auto
    }

    .swiper-container-autoheight .swiper-wrapper {
        align-items: flex-start;
        transition-property: transform,height
    }

    .swiper-container-3d {
        perspective: 1200px
    }

    .swiper-container-3d .swiper-cube-shadow,.swiper-container-3d .swiper-slide,.swiper-container-3d .swiper-slide-shadow-bottom,.swiper-container-3d .swiper-slide-shadow-left,.swiper-container-3d .swiper-slide-shadow-right,.swiper-container-3d .swiper-slide-shadow-top,.swiper-container-3d .swiper-wrapper {
        transform-style: preserve-3d
    }

    .swiper-container-3d .swiper-slide-shadow-bottom,.swiper-container-3d .swiper-slide-shadow-left,.swiper-container-3d .swiper-slide-shadow-right,.swiper-container-3d .swiper-slide-shadow-top {
        height: 100%;
        left: 0;
        pointer-events: none;
        position: absolute;
        top: 0;
        width: 100%;
        z-index: 10
    }

    .swiper-container-3d .swiper-slide-shadow-left {
        background-image: linear-gradient(270deg,rgba(0,0,0,.5),transparent)
    }

    .swiper-container-3d .swiper-slide-shadow-right {
        background-image: linear-gradient(90deg,rgba(0,0,0,.5),transparent)
    }

    .swiper-container-3d .swiper-slide-shadow-top {
        background-image: linear-gradient(0deg,rgba(0,0,0,.5),transparent)
    }

    .swiper-container-3d .swiper-slide-shadow-bottom {
        background-image: linear-gradient(180deg,rgba(0,0,0,.5),transparent)
    }

    .swiper-container-css-mode>.swiper-wrapper {
        -ms-overflow-style: none;
        overflow: auto;
        scrollbar-width: none
    }

    .swiper-container-css-mode>.swiper-wrapper::-webkit-scrollbar {
        display: none
    }

    .swiper-container-css-mode>.swiper-wrapper>.swiper-slide {
        scroll-snap-align: start start
    }

    .swiper-container-horizontal.swiper-container-css-mode>.swiper-wrapper {
        scroll-snap-type: x mandatory
    }

    .swiper-container-vertical.swiper-container-css-mode>.swiper-wrapper {
        scroll-snap-type: y mandatory
    }

    .Hero {
        background: #111;
        color: #fff
    }

    .Hero,.Hero .fp-tableCell {
        transform: translateZ(0);
        transition: height .1s linear
    }

    @media(hover: hover) {
        .Hero,.Hero .fp-tableCell {
            height:100vh!important
        }
    }

    @media(hover: none) {
        .Hero,.Hero .fp-tableCell {
            height:var(--hero-height)
        }
    }

    .Hero-inner {
        align-items: flex-start;
        display: flex;
        flex-direction: column;
        height: 100%;
        justify-content: center;
        padding: 130px;
        perspective: 1500px;
        perspective-origin: 50%;
        transition: height .1s linear
    }

    @media(hover: hover) {
        .Hero-inner {
            height:100vh!important
        }
    }

    @media(hover: none) {
        .Hero-inner {
            height:var(--hero-height)
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .Hero-inner {
            padding:90px
        }
    }

    @media(max-width: 992px) {
        .Hero-inner {
            padding:50px 8.6vw
        }
    }

    @media(min-width: 767px)and (max-width:700px)and (orientation:landscape) {
        .Hero-inner {
            padding:50px 30px 70px
        }
    }

    .Hero-innerer>* {
        opacity: 1;
        text-shadow: 0 0 100px rgba(0,0,0,.4);
        transform: translateY(200px) rotateY(40deg);
        transform-origin: center center;
        transition: opacity .5s cubic-bezier(.895,.03,.685,.22),transform 1.6s cubic-bezier(.165,.84,.44,1)
    }

    .fullpage-loaded .Hero-innerer>:first-child {
        opacity: 1;
        transform: translateY(0) rotateY(0);
        transition-delay: 0s
    }

    .fullpage-loaded .Hero-innerer>:nth-child(2) {
        opacity: 1;
        transform: translateY(0) rotateY(0);
        transition-delay: .2s
    }

    .fullpage-loaded .Hero-innerer>:nth-child(3) {
        opacity: 1;
        transform: translateY(0) rotateY(0);
        transition-delay: .4s
    }

    .fullpage-loaded .Hero-innerer>:nth-child(4) {
        opacity: 1;
        transform: translateY(0) rotateY(0);
        transition-delay: .6s
    }

    .Hero-video {
        opacity: 1;
        transform: scale(1.3)
    }

    .fullpage-loaded .Hero-video {
        animation: fade-in .6s cubic-bezier(.895,.03,.685,.22) .3s forwards,transform-out 2.4s cubic-bezier(.165,.84,.44,1) .3s forwards
    }

    .Hero-title {
        font-size: 120px;
        font-weight: 400;
        letter-spacing: -.01em;
        line-height: .9
    }

    @media(max-width: 1440px) {
        .Hero-title {
            font-size:3.75rem;
            letter-spacing: -.4px
        }
    }

    @media(max-width: 576px) {
        .Hero-title {
            font-size:40px
        }
    }

    .Hero-inner.has-news .Hero-title {
        padding-bottom: 50px
    }

    .Hero-label {
        display: block;
        font-size: 18px;
        font-weight: 500;
        letter-spacing: .8px;
        letter-spacing: .04em;
        line-height: 1.4;
        padding-bottom: 2em;
        text-transform: uppercase
    }

    .Hero--about .Hero-label,.Hero--home .Hero-label {
        padding-top: 3em;
        position: absolute
    }

    @media(max-width: 1440px) {
        .Hero-label {
            font-size:.75rem
        }
    }

    .Hero-cta {
        align-items: center;
        color: #fff;
        display: flex;
        font-weight: 300;
        padding-top: 1.875rem;
        position: absolute;
        -webkit-text-decoration: none;
        text-decoration: none
    }

    @media(max-width: 1440px) {
        .Hero-cta {
            font-size:.8125rem
        }
    }

    .Hero-cta:before {
        background: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4NCjxzdmcgd2lkdGg9IjI0cHgiIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPg0KICAgIDwhLS0gR2VuZXJhdG9yOiBTa2V0Y2ggNDkuMyAoNTExNjcpIC0gaHR0cDovL3d3dy5ib2hlbWlhbmNvZGluZy5jb20vc2tldGNoIC0tPg0KICAgIDx0aXRsZT5Hcm91cDwvdGl0bGU+DQogICAgPGRlc2M+Q3JlYXRlZCB3aXRoIFNrZXRjaC48L2Rlc2M+DQogICAgPGRlZnM+PC9kZWZzPg0KICAgIDxnIGlkPSJQYWdlLTEiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBmaWxsPSJub25lIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiPg0KICAgICAgICA8ZyBpZD0iR3JvdXAiIGZpbGw9IiNGRkZGRkYiIGZpbGwtcnVsZT0ibm9uemVybyI+DQogICAgICAgICAgICA8cGF0aCBkPSJNMTIsMjQgQzUuMzcyNTgzLDI0IDAsMTguNjI3NDE3IDAsMTIgQzAsNS4zNzI1ODMgNS4zNzI1ODMsMCAxMiwwIEMxOC42Mjc0MTcsMCAyNCw1LjM3MjU4MyAyNCwxMiBDMjQsMTguNjI3NDE3IDE4LjYyNzQxNywyNCAxMiwyNCBaIE0xMCw4IEwxMCwxNiBMMTYsMTIgTDEwLDggWiIgaWQ9IkNvbWJpbmVkLVNoYXBlIj48L3BhdGg+DQogICAgICAgIDwvZz4NCiAgICA8L2c+DQo8L3N2Zz4=) no-repeat 0 0/100% auto;
        content: "";
        height: 24px;
        margin-right: 10px;
        width: 24px
    }

    @media(max-width: 1440px) {
        .Hero-cta:before {
            height:21px;
            width: 21px
        }
    }

    .Hero-news {
        align-content: space-between;
        align-items: flex-end;
        background-size: cover;
        border-radius: 5px;
        bottom: 20px;
        cursor: pointer;
        display: flex;
        flex-wrap: wrap;
        height: 180px;
        overflow: hidden;
        padding: 15px;
        right: 50px;
        transform: translateY(0);
        transition: transform 1s cubic-bezier(.165,.84,.44,1) 0.8s;
        width: 220px;
        z-index: 1
    }

    @media(max-width: 767px) {
        .Hero-news {
            align-items:center;
            background-color: #111;
            bottom: calc(20px + env(safe-area-inset-top));
            height: auto;
            left: 10px;
            right: 10px;
            width: auto
        }
    }

    .Hero-news:hover .Hero-newsImg {
        transform: scale(1.07)
    }

    .Hero-news>* {
        position: relative;
        z-index: 1
    }

    .Hero-news:before {
        background-image: linear-gradient(180deg,hsla(0,0%,7%,0),#111);
        border-radius: 5px;
        bottom: 0;
        content: "";
        left: 0;
        opacity: .7;
        position: absolute;
        right: 0;
        top: 0
    }

    .Hero-newsLabelWrapper {
        display: flex
    }

    @media(min-width: 768px) {
        .Hero-newsLabelWrapper {
            width:100%
        }
    }

    .Hero-newsLabel {
        background-color: #fff;
        border-radius: 100px;
        color: #111;
        font-size: .5rem;
        font-weight: 500;
        padding: 3px 7px;
        text-transform: uppercase
    }

    @media(max-width: 576px) {
        .Hero-newsLabel {
            font-size:6px
        }
    }

    .Hero-newsImg {
        height: 100%;
        left: 0;
        -o-object-fit: cover;
        object-fit: cover;
        position: absolute;
        top: 0;
        
        width: 100%;
        z-index: -1
    }

    @media(max-width: 767px) {
        .Hero-newsImg {
            display:none
        }
    }

    .Hero-newsTitle {
        flex: 1;
        letter-spacing: -.03em;
        padding-right: 10px
    }

    @media(max-width: 767px) {
        .Hero-newsTitle {
            padding-left:10px
        }
    }

    @media(max-width: 576px) {
        .Hero-newsTitle {
            font-size:.75rem
        }
    }

    @media(min-width: 768px) {
        .Hero-newsIcon {
            top:-4px
        }
    }

    .HiringBanner {
        align-items: center;
        -webkit-backdrop-filter: blur(8px);
        backdrop-filter: blur(8px);
        background-color: hsla(0,0%,7%,.4);
        color: #fff;
        cursor: pointer;
        display: flex;
        font-weight: 700;
        font-weight: 500;
        justify-content: space-between;
        left: 0;
        position: fixed;
        right: 0;
        text-transform: uppercase;
        top: 0;
        z-index: 20
    }

    .HiringBanner,.HiringBanner.v-enter-active,.HiringBanner.v-leave-active {
        transition: transform 1s cubic-bezier(.77,0,.175,1)
    }

    @media(max-width: 992px) {
        .HiringBanner {
            font-size:.625rem;
            height: 32px
        }
    }

    @media(min-width: 993px) {
        .HiringBanner {
            font-size:.6875rem;
            height: 36px
        }
    }

    .HiringBanner.v-enter,.HiringBanner.v-leave-to {
        transform: translateY(-100%)
    }

    #fp-nav {
        opacity: 1;
        transition: opacity .4s linear
    }

    @media(max-width: 1439px) {
        #fp-nav {
            display:none
        }
    }

    @media(min-width: 1440px) {
        #fp-nav {
            color:#000;
            font-size: 10px;
            left: 35px;
            margin-top: 0!important;
            position: fixed;
            top: 50%;
            transform: translateY(-50%);
            z-index: 100
        }

        .sidebar-open #fp-nav {
            opacity: 0.5;
            pointer-events: none
        }

        #fp-nav li {
            margin: .7vh 0
        }

        #fp-nav a {
            align-items: center;
            color: #fff;
            display: flex;
            font-weight: 800;
            height: 3vh;
            overflow: hidden;
            -webkit-text-decoration: none;
            text-decoration: none;
            text-transform: uppercase
        }

        #fp-nav a[href="#Footer"] {
            display: none
        }

        .fp-viewing-Softwares #fp-nav a {
            color: #111
        }

        .fp-viewing-Softwares #fp-nav a:before {
            background-color: #111
        }

        #fp-nav a:before {
            background-color: #fff;
            left: -15px;
            opacity: .3;
            transition: opacity .3s linear;
            width: 2px;
            will-change: opacity
        }

        #fp-nav a:after,#fp-nav a:before {
            content: "";
            display: block;
            height: inherit;
            position: absolute
        }

        #fp-nav a:after {
            left: -30px;
            right: 0
        }

        #fp-nav a .fp-sr-only {
            letter-spacing: 1px;
            transform: translateX(-100%);
            transition: transform .8s cubic-bezier(.86,0,.07,1);
            will-change: transform
        }

        #fp-nav a.active .fp-sr-only,#fp-nav a:hover .fp-sr-only {
            transform: translateX(0);
            transition-delay: .6s
        }

        #fp-nav a.active:before,#fp-nav a:hover:before {
            opacity: 1
        }

        #fp-nav a:hover .fp-sr-only {
            transition-delay: 0s
        }

        #fp-nav .fp-tooltip {
            display: none
        }
    }

    .Loader:after,.Loader:before {
        content: "";
        display: block;
        height: 2px;
        left: 50%;
        position: absolute;
        top: 50%;
        transform: translate(-50%,-50%);
        transform-origin: left;
        width: 200px;
        z-index: -1
    }

    .Loader:before {
        background: hsla(0,0%,100%,.2)
    }

    .Loader:after {
        animation: video-loading 2s ease infinite;
        background: #fff
    }

    .Loader--darker {
        z-index: 0
    }

    .Loader--darker:before {
        background: rgba(0,0,0,.2)
    }

    .Loader--darker:after {
        background: #000
    }

    .Modal {
        align-content: center;
        background-color: rgba(0,0,0,.8);
        display: flex;
        height: 100vh;
        justify-content: center;
        left: 0;
        overflow: auto;
        top: 0;
        width: 100vw;
        z-index: 100
    }

    @media(max-width: 992px) {
        .Modal {
            position:fixed
        }
    }

    @media(min-width: 993px) {
        .Modal {
            position:absolute
        }
    }

    .Modal.v-enter-active,.Modal.v-leave-active {
        transition: opacity .3s;
        will-change: opacity
    }

    .Modal.v-enter,.Modal.v-leave-to {
        opacity: 0
    }

    .Modal-content {
        background: #111;
        margin: auto;
        padding-bottom: 45%;
        position: relative;
        width: 80vw
    }

    .Modal-content.v-enter-active,.Modal-content.v-leave-active {
        transition: transform .8s cubic-bezier(.165,.84,.44,1) .4s,opacity .3s linear .4s;
        will-change: transform,opacity
    }

    .Modal-content.v-enter,.Modal-content.v-leave-to {
        opacity: 0;
        transform: scale(.9)
    }

    .Modal-video {
        height: 100%;
        left: 0;
        position: absolute;
        top: 0;
        width: 100%
    }

    .SubscribeForm.is-loading {
        position: relative
    }

    .SubscribeForm.is-loading:after {
        animation: form-loading 2s cubic-bezier(.77,0,.175,1) forwards;
        background-color: #1efd8d;
        content: "";
        height: 1px;
        position: absolute;
        top: 100%;
        width: 100%
    }

    .SubscribeForm.is-loading .SubscribeForm-submit {
        cursor: auto;
        pointer-events: none
    }

    .SubscribeForm-fields {
        display: flex;
        gap: 2px;
        height: 40px;
        position: relative
    }

    .SubscribeForm-label {
        display: block;
        margin-bottom: .9375rem
    }

    .SubscribeForm-input {
        background-color: hsla(0,0%,100%,.05);
        color: #fff;
        flex: 1;
        font-family: inherit;
        font-size: 12px;
        font-weight: 300;
        height: 100%;
        min-width: 100px;
        padding-left: 15px;
        padding-right: 15px
    }

    @media(max-width: 576px) {
        .SubscribeForm-input {
            max-width:220px
        }
    }

    @media(min-width: 577px) {
        .SubscribeForm-input {
            width:220px
        }
    }

    .SubscribeForm-input:not(:-moz-placeholder-shown)~.SubscribeForm-status {
        background-color: hsla(0,0%,100%,.2)
    }

    .SubscribeForm-input:not(:placeholder-shown)~.SubscribeForm-status {
        background-color: hsla(0,0%,100%,.2)
    }

    .SubscribeForm-input:not(:-moz-placeholder-shown):valid+.SubscribeForm-submit {
        color: #1efd8d;
        cursor: pointer;
        pointer-events: auto
    }

    .SubscribeForm-input:not(:placeholder-shown):valid+.SubscribeForm-submit {
        color: #1efd8d;
        cursor: pointer;
        pointer-events: auto
    }

    .has-error .SubscribeForm-input:not(:-moz-placeholder-shown):valid+.SubscribeForm-submit {
        color: hsla(0,0%,100%,.15)
    }

    .has-error .SubscribeForm-input:not(:placeholder-shown):valid+.SubscribeForm-submit {
        color: hsla(0,0%,100%,.15)
    }

    .SubscribeForm-input:not(:-moz-placeholder-shown):valid+.SubscribeForm-submit:hover {
        color: #111
    }

    .SubscribeForm-input:not(:placeholder-shown):valid+.SubscribeForm-submit:hover {
        color: #111
    }

    .SubscribeForm-input:not(:-moz-placeholder-shown):valid~.SubscribeForm-status {
        background-color: #1efd8d
    }

    .SubscribeForm-input:not(:placeholder-shown):valid~.SubscribeForm-status {
        background-color: #1efd8d
    }

    .SubscribeForm-submit {
        background-color: hsla(0,0%,100%,.05);
        color: hsla(0,0%,100%,.15);
        font-family: inherit;
        font-size: 10px;
        font-weight: 500;
        height: 100%;
        letter-spacing: 1px;
        padding-left: 20px;
        padding-right: 20px;
        pointer-events: none;
        position: relative;
        text-transform: uppercase;
        transition: color .05s linear .1s
    }

    .SubscribeForm-submit:before {
        background-color: #1efd8d;
        bottom: 0;
        content: "";
        display: block;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        transform: scaleX(0);
        transform-origin: right;
        transition: transform .25s cubic-bezier(.77,0,.175,1);
        will-change: transform
    }

    .SubscribeForm-submit:hover {
        color: #111
    }

    .SubscribeForm-submit:hover:before {
        transform: scaleX(1);
        transform-origin: left
    }

    .SubscribeForm-status {
        border-radius: 100%;
        height: 4px;
        position: absolute;
        right: calc(100% + 10px);
        top: 50%;
        transform: translateY(-50%);
        transition: background-color .15s linear;
        width: 4px
    }

    .has-error .SubscribeForm-status {
        background-color: #ff3030!important
    }

    .SubscribeForm-feedback {
        font-size: 11px;
        left: 2px;
        position: absolute;
        top: calc(100% + 10px)
    }

    .SubscribeForm-feedback.v-enter-active,.SubscribeForm-feedback.v-leave-active {
        transition: opacity .2s linear,transform .6s cubic-bezier(.165,.84,.44,1)
    }

    .SubscribeForm-feedback.v-enter,.SubscribeForm-feedback.v-leave-to {
        opacity: 0;
        transform: translateY(-10px)
    }

    .SubscribeForm-feedback a {
        color: currentColor;
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .SubscribeForm-feedback--success {
        color: #1efd8d
    }

    .SubscribeForm-feedback--error {
        color: #ff3030
    }

    .Gallery {
        background-color: #f4f4f4;
        padding-bottom: 56.25%;
        position: relative
    }

    .Gallery-mainImg {
        position: absolute;
        z-index: 1
    }

    .Gallery-mainImg.v-enter-active,.Gallery-mainImg.v-leave-active {
        transition: opacity .2s linear
    }

    .Gallery-mainImg.v-enter,.Gallery-mainImg.v-enter-leave-to {
        opacity: 0
    }

    .Gallery-thumbnails {
        grid-gap: 5px;
        bottom: 10px;
        display: grid;
        grid-auto-columns: max-content;
        grid-auto-flow: column;
        position: absolute;
        right: 10px;
        z-index: 2
    }

    .Gallery-thumbnailsImg {
        background-color: #fff
    }

    .Gallery-thumbnailsImg.is-active,.Gallery-thumbnailsImg:hover {
        cursor: pointer
    }

    .Gallery-thumbnailsImg.is-active img,.Gallery-thumbnailsImg:hover img {
        opacity: 1;
        transition-duration: .05s
    }

    .Gallery-thumbnailsImg img {
        height: 75px;
        opacity: .6;
        transition: opacity .3s linear
    }

    @media(max-width: 576px) {
        .Gallery-thumbnailsImg img {
            height:45px
        }
    }

    .MainLogo {
        color: #111;
        cursor: pointer;
        transition: color .4s cubic-bezier(.86,0,.07,1) .4s,opacity .4s cubic-bezier(.86,0,.07,1),transform .4s cubic-bezier(.165,.84,.44,1)
    }

    .fp-viewing-Benefits .MainLogo,.fp-viewing-BoardMembers .MainLogo,.fp-viewing-Careers-Footer .MainLogo,.fp-viewing-Cost .MainLogo,.fp-viewing-Footer .MainLogo,.fp-viewing-Meet .MainLogo,.fp-viewing-Process .MainLogo,.fp-viewing-Softwares .MainLogo,.fp-viewing-Speed .MainLogo,.fp-viewing-Technology .MainLogo {
        color: #111
    }

    @media(max-width: 992px) {
        .fp-viewing-Footer .MainLogo {
            opacity:0
        }
    }

    body:not(.sidebar-open) .MainLogo {
        pointer-events: all
    }

    [class*=page-projects-slug] .MainLogo {
        pointer-events: none!important;
        visibility: hidden
    }

    .custom-transition .MainLogo {
        opacity: 0;
        transition-delay: .4s,.4s,0s
    }

    .MainLogo-inline {
        color: #fff;
        overflow: hidden;
        position: relative;
        top: -8px;
        transition: width .7s cubic-bezier(.86,0,.07,1) 1.1s;
        width: 0
    }

    .first-load .MainLogo-inline {
        width: 77px
    }

    [class*=fp-viewing-]:not(.fp-viewing-Leko) .MainLogo-inline {
        transition-delay: .2s;
        transition-duration: .4s;
        width: 0
    }

    [class*=page-projects-slug] .MainLogo-inline {
        transition-delay: 0s;
        width: 0
    }

    .MainLogo-inline svg {
        width: 77px
    }

    @media(max-width: 1440px) {
        .MainLogo-inline svg {
            width:60px
        }
    }

    .fp-viewing-Leko.fullpage-loaded .MainLogo-inline {
        width: 77px
    }

    @media(max-width: 1440px) {
        .fp-viewing-Leko.fullpage-loaded .MainLogo-inline {
            width:60px
        }
    }

    .MainLogo-L {
        height: 31px;
        opacity: 1;
        position: absolute;
        top: 35px;
        transition: opacity .1s linear .5s;
        width: 22px;
        will-change: opacity
    }

    .fp-viewing-Leko .MainLogo-L,body:not([class]) .MainLogo-L {
        opacity: 1;
        transition: none!important
    }

    @media(min-width: 577px)and (max-width:992px) {
        .MainLogo-L {
            height:27px;
            width: 19px
        }
    }

    @media(max-width: 576px) {
        .MainLogo-L {
            height:24px;
            top: 25px;
            width: 17px
        }
    }

    body[class*=fp-viewing-]:not(.fp-viewing-Leko) .MainLogo-L {
        opacity: 1
    }

    .LangSwitcher {
        color: hsla(0,0%,100%,.5);
        display: flex
    }

    .LangSwitcher-item:not(:first-child):before {
        content: "/";
        display: inline-flex;
        margin-left: .5em;
        margin-right: .5em
    }

    .LangSwitcher-link {
        color: currentColor;
        transition: color .3s linear
    }

    .LangSwitcher-link.nuxt-link-active,.LangSwitcher-link:hover {
        color: #111
    }

    .PlusMenu {
        color: #1efd8d;
        cursor: pointer;
        height: 22px;
        position: relative;
        transition: color .4s cubic-bezier(.86,0,.07,1) .4s,opacity .4s cubic-bezier(.86,0,.07,1),transform .4s cubic-bezier(.165,.84,.44,1);
        width: 22px
    }

    @media(max-width: 576px) {
        .PlusMenu {
            height:17px;
            width: 17px
        }
    }

    .PlusMenu:hover {
        color: #fff;
        transition-delay: 0s!important
    }

    .PlusMenu:after {
        content: "";
        height: 45px;
        left: 50%;
        position: absolute;
        top: 50%;
        transform: translate(-50%,-50%);
        width: 50px
    }

    body:not(.sidebar-open) .PlusMenu {
        pointer-events: all
    }

    .PlusMenu.is-open {
        transform: rotate(45deg)
    }

    .menu-is-open .PlusMenu {
        color: #1efd8d!important;
        transition-delay: 0s!important;
        transition-duration: 0s,.4s,.4s!important
    }

    .menu-is-open .PlusMenu:hover {
        color: #fff!important
    }

    .fp-viewing-About .PlusMenu,.fp-viewing-Benefits .PlusMenu,.fp-viewing-Footer .PlusMenu,.fp-viewing-Founder .PlusMenu,.fp-viewing-Process .PlusMenu,.fp-viewing-Robotics .PlusMenu,.fp-viewing-System .PlusMenu {
        color: #111
    }

    .PlusMenu-icon {
        height: 100%;
        width: 100%
    }

    .DragCursor {
        align-items: center;
        background-color: #fff;
        border-radius: 100%;
        color: #111;
        display: flex;
        font-size: 1.125rem;
        height: 120px;
        justify-content: center;
        pointer-events: none;
        position: absolute;
        transition: opacity .2s linear,background-color .5s linear;
        width: 120px;
        z-index: 10
    }

    @media(hover: none) {
        .DragCursor {
            font-size:.75rem;
            height: 70px;
            left: 205px;
            top: 300px;
            width: 70px
        }
    }

    .DragCursor.is-hidden {
        opacity: 1;
    }

    .DragCursor.is-hover {
        background-color: #000
    }

    .DragCursor.is-hover:after,.DragCursor.is-hover:before {
        opacity: 1;
    }

    @media(hover: none) {
        .DragCursor.has-dragged-on-mobile {
            opacity:1;
        }
    }

    .DragCursor:after,.DragCursor:before {
        background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg viewBox='0 0 7 12' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M6 1 1 6l5 5' stroke='%23fff' stroke-width='1.5' fill='none' fill-rule='evenodd'/%3E%3C/svg%3E");
        content: "";
        display: block;
        height: 10px;
        position: absolute;
        transition: opacity .5s linear;
        width: 6px
    }

    .DragCursor:before {
        right: calc(100% + 18px)
    }

    @media(hover: none) {
        .DragCursor:before {
            right:calc(100% + 10px)
        }
    }

    .DragCursor:after {
        left: calc(100% + 18px);
        transform: scaleX(-1)
    }

    @media(hover: none) {
        .DragCursor:after {
            left:calc(100% + 10px)
        }
    }

    .DragCursor-txt {
        height: 20px;
        overflow: hidden;
        position: relative;
        text-align: center;
        width: 100%
    }

    @media(hover: none) {
        .DragCursor-txt {
            height:14px
        }
    }

    .DragCursor-close,.DragCursor-drag,.DragCursor-show {
        left: 0;
        position: absolute;
        width: 100%
    }

    .DragCursor-close.v-enter-active,.DragCursor-close.v-leave-active,.DragCursor-drag.v-enter-active,.DragCursor-drag.v-leave-active,.DragCursor-show.v-enter-active,.DragCursor-show.v-leave-active {
        transition-duration: .35s;
        transition-property: transform
    }

    .DragCursor-close.v-enter-active,.DragCursor-drag.v-enter-active,.DragCursor-show.v-enter-active {
        transition-delay: .25s;
        transition-timing-function: cubic-bezier(.23,1,.32,1)
    }

    .DragCursor-close.v-leave-active,.DragCursor-drag.v-leave-active,.DragCursor-show.v-leave-active {
        transition-timing-function: cubic-bezier(.755,.05,.855,.06)
    }

    .DragCursor-close.v-leave-to,.DragCursor-drag.v-leave-to,.DragCursor-show.v-leave-to {
        transform: translateY(-100%)
    }

    .DragCursor-close.v-enter,.DragCursor-drag.v-enter,.DragCursor-show.v-enter {
        transform: translateY(100%)
    }

    .SliderProgressBar {
        height: 3px;
        left: 50%;
        opacity: 1;;
        position: absolute;
        transform: translateX(-50%);
        width: 400px;
        z-index: 5
    }

    @media(min-width: 577px) {
        .SliderProgressBar {
            bottom:30px
        }
    }

    @media(max-width: 576px) {
        .SliderProgressBar {
            bottom:40px
        }
    }

    .SliderProgressBar--light {
        background-color: hsla(0,0%,100%,.1)
    }

    .SliderProgressBar--light .SliderProgressBar-fill {
        background-color: #fff
    }

    .SliderProgressBar--dark {
        background-color: hsla(0,0%,7%,.1)
    }

    .SliderProgressBar--dark .SliderProgressBar-fill {
        background-color: hsla(0,0%,7%,.5)
    }

    @media(max-width: 1440px) {
        .SliderProgressBar {
            bottom:30px;
            width: 300px
        }
    }

    @media(max-width: 992px) {
        .SliderProgressBar {
            bottom:40px
        }
    }

    @media(max-width: 767px) {
        .SliderProgressBar {
            bottom:30px
        }
    }

    .complete .SliderProgressBar {
        opacity: 1;
        transition: opacity .8s cubic-bezier(.77,0,.175,1) 2.2s
    }

    .SliderProgressBar-fill {
        background-color: currentColor;
        height: 100%;
        position: absolute;
        top: 0;
        transform-origin: left;
        transition: transform .8s cubic-bezier(.77,0,.175,1);
        width: 100%
    }

    @media(max-width: 992px) {
        .HQ-image {
            height:70vw
        }
    }

    .JobCTA {
        align-items: center;
        background-color: #f4f4f4;
        bottom: 0;
        color: #111;
        cursor: pointer;
        display: flex;
        font-size: 2.5rem;
        justify-content: space-between;
        left: 0;
        letter-spacing: -.02em;
        opacity: 1;
        padding: calc(2vw + 50px) 130px;
        position: absolute;
        right: 0;
        transform: translateY(100%) rotateY(0);
        transition-delay: 1.2s!important
    }

    @media(max-width: 1440px) {
        .JobCTA {
            padding-left:90px;
            padding-right: 90px
        }
    }

    @media(max-width: 992px) {
        .JobCTA {
            padding-left:8.6vw;
            padding-right: 8.6vw
        }
    }

    @media(max-width: 576px) {
        .JobCTA {
            font-size:1.25rem;
            padding-bottom: 34px;
            padding-top: 34px
        }
    }

    .JobCTA:hover .JobCTA-label:after {
        transform: scaleX(1);
        transform-origin: left;
        transition-timing-function: cubic-bezier(.23,1,.32,1)
    }

    .JobCTA-label {
        position: relative
    }

    .JobCTA-label:after {
        background: currentColor;
        content: "";
        height: 1.4px;
        left: 0;
        position: absolute;
        right: 0;
        top: 100%;
        transform: scaleX(0);
        transform-origin: right;
        transition: transform .6s cubic-bezier(.755,.05,.855,.06)
    }

    @media(min-width: 992px) {
        .JobCTA-label:after {
            height:3px
        }
    }

    .JobCTA-icon {
        margin-left: 40px;
        transform: scaleY(-1)
    }

    @media(max-width: 576px) {
        .JobCTA-icon {
            width:20px
        }
    }

    .Job-title {
        cursor: pointer
    }

    .Job-newLabel {
        display: flex;
        overflow: hidden;
        transition: width 1s cubic-bezier(.86,0,.07,1) 2.5s;
        width: 0;
        will-change: width
    }

    .active .Job-newLabel,.complete .Job-newLabel {
        width: 40px
    }

    [class*=fr] .active .Job-newLabel,[class*=fr] .complete .Job-newLabel {
        width: 58px
    }

    .Job-newLabelText {
        background: #1efd8d;
        border-radius: 1px;
        color: #000;
        font-size: .625rem;
        padding: 1px 6px
    }

    .Job-category {
        color: #1efd8d
    }

    .Job-extract {
        color: #111;
        cursor: pointer;
        display: inline-block!important
    }

    .Job-extract.v-enter-active,.Job-extract.v-leave-active {
        position: relative;
        transition: transform 1s cubic-bezier(1,0,0,1);
        will-change: transform
    }

    .Job-extract.v-enter-active:after,.Job-extract.v-leave-active:after {
        background: #fff;
        bottom: 0;
        content: "";
        display: block;
        position: absolute;
        right: 0;
        top: 0;
        transform: scaleX(0);
        transform-origin: right;
        transition: transform 1s cubic-bezier(1,0,0,1);
        width: 100%;
        z-index: 1
    }

    .Job-extract.v-enter-active,.Job-extract.v-enter-active:after {
        transition-delay: .6s
    }

    .is-safari .Job-extract.v-enter-active,.is-safari .Job-extract.v-enter-active:after {
        transition-delay: 0s
    }

    .Job-extract.v-enter:after,.Job-extract.v-leave-to:after {
        transform: scaleX(1)
    }

    .Job-extract[style*=display] {
        opacity: 1;
    }

    .Job-extract:hover .Job-title {
        color: #1efd8d
    }

    .Job-subhead {
        align-items: center;
        display: flex;
        overflow: hidden
    }

    .Job-link {
        border: 1px solid #1efd8d;
        color: #1efd8d;
        display: inline-block;
        font-size: .75rem;
        font-weight: 300;
        padding: 12px 70px;
        -webkit-text-decoration: none;
        text-decoration: none;
        text-transform: uppercase
    }

    @media(max-width: 767px) {
        .Job-link--desk {
            display:none
        }
    }

    @media(min-width: 768px) {
        .Job-link--mobile {
            display:none
        }
    }

    .Job-link:hover {
        background: #1efd8d;
        color: #111
    }

    @media(max-width: 576px) {
        .Job-link {
            text-align:center;
            width: 100%
        }
    }

    .Job-details {
        transform: translateY(-40px)
    }

    @media(min-width: 768px) {
        .Job-details {
            display:flex
        }
    }

    .Job-details.v-enter-active,.Job-details.v-leave-active {
        max-height: 220vh;
        opacity: 1;
        overflow: hidden;
        transition: max-height .9s cubic-bezier(.77,0,.175,1),transform .9s cubic-bezier(.77,0,.175,1),opacity .6s cubic-bezier(.77,0,.175,1);
        will-change: max-height,transform,opacity
    }

    .Job-details.v-enter-active {
        transition-delay: .9s,.9s,.9s
    }

    .is-safari .Job-details.v-enter-active {
        transition-delay: 0s
    }

    .Job-details.v-enter,.Job-details.v-leave-to {
        max-height: 0;
        opacity: 1;;
        transform: translateY(40px)
    }

    .Job-side {
        flex: 1;
        margin-right: 7.3vw;
        max-width: 320px
    }

    @media(max-width: 1440px) {
        .Job-side {
            max-width:280px
        }
    }

    @media(max-width: 768px) {
        .Job-side {
            margin-right:6vw;
            max-width: 240px
        }
    }

    @media(max-width: 767px) {
        .Job-side {
            margin-bottom:1.875rem;
            max-width: none
        }
    }

    .Job-sideTitle {
        color: #111;
        display: block;
        opacity: .3;
        text-transform: uppercase
    }

    .Job-main {
        flex: 1
    }

    .Jobs {
        background: #fff;
        color: #111
    }

    .Jobs-inner {
        padding: 6vh 7.6vw
    }

    @media(max-width: 992px) {
        .Jobs-inner {
            padding-bottom:15vw;
        }
    }

    @media(min-width: 993px) {
        .Jobs-inner {
            min-height:101vh;
            padding-bottom: 15vh;
        }
    }

    .Jobs-filter {
        display: block;
        margin-bottom: 5rem;
        opacity: 0;
        position: relative;
        transform: scale(.9) translateY(120px);
        transform-origin: top;
        transition: opacity .3s linear,transform 1s cubic-bezier(.165,.84,.44,1);
        -webkit-user-select: none;
        -moz-user-select: none;
        user-select: none;
        will-change: opacity,transform;
        z-index: 1
    }

    @media(max-width: 1440px) {
        .Jobs-filter {
            margin-bottom:3.125rem
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-filter {
            transition-delay:.55s,.55s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-filter {
            transition-delay:1s,1s
        }
    }

    .active .Jobs-filter,.complete .Jobs-filter {
        opacity: 1;
        transform: scale(1) translateY(0)
    }

    .Jobs-filterCurrent {
        border-bottom: 1px solid hsla(0,0%,100%,.2);
        color: #1efd8d;
        cursor: pointer;
        display: block;
        padding: 6px 0
    }

    .Jobs-filterCurrent.is-open:after {
        transform: translate(-3px,calc(-50% + 3px)) rotate(-135deg)
    }

    .Jobs-filterCurrent:after {
        border: solid #1efd8d;
        border-width: 0 1px 1px 0;
        content: "";
        display: inline-block;
        padding: 3px;
        position: absolute;
        right: 0;
        top: 50%;
        transform: translate(-3px,-50%) rotate(45deg)
    }

    .Jobs-filterList {
        background: #161616;
        border-radius: 2px;
        box-shadow: 0 8px 0 0 #111;
        display: block;
        font-size: .8125rem;
        padding: 0 15px;
        position: absolute;
        top: calc(100% + 10px);
        width: 100%
    }

    .Jobs-filterList.v-enter-active,.Jobs-filterList.v-leave-active {
        transform: translateY(0) scale(1);
        transform-origin: bottom;
        transition: opacity .3s cubic-bezier(.165,.84,.44,1),transform .6s cubic-bezier(.165,.84,.44,1)
    }

    .Jobs-filterList.v-enter,.Jobs-filterList.v-leave-to {
        opacity: 0;
        pointer-events: none;
        transform: translateY(-20px) scale(1.02)
    }

    .Jobs-filterListItem {
        border-bottom: 1px solid #111;
        cursor: pointer;
        display: block;
        padding: 14px 0
    }

    .Jobs-filterListItem:hover {
        color: #1efd8d
    }

    .Jobs-listItem {
        margin-bottom: 0;
        opacity: 0;
        transform: translateY(140px);
        transition: opacity .3s cubic-bezier(.895,.03,.685,.22),transform 1s cubic-bezier(.165,.84,.44,1);
        will-change: transform,opacity
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(0) {
            transition-delay:1.1s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(0) {
            transition-delay:.65s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:first-child {
            transition-delay:1.22s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:first-child {
            transition-delay:.77s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(2) {
            transition-delay:1.34s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(2) {
            transition: delay 0.89s;

        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(3) {
            transition-delay:1.46s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(3) {
            transition-delay:1.01s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(4) {
            transition-delay:1.58s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(4) {
            transition-delay:1.13s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(5) {
            transition-delay:1.7s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(5) {
            transition-delay:1.25s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(6) {
            transition-delay:1.82s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(6) {
            transition-delay:1.37s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(7) {
            transition-delay:1.94s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(7) {
            transition-delay:1.49s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(8) {
            transition-delay:2.06s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(8) {
            transition-delay:1.61s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(9) {
            transition-delay:2.18s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(9) {
            transition-delay:1.73s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(10) {
            transition-delay:2.3s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(10) {
            transition-delay:1.85s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(11) {
            transition-delay:2.42s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(11) {
            transition-delay:1.97s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(12) {
            transition-delay:2.54s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(12) {
            transition-delay:2.09s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(13) {
            transition-delay:2.66s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(13) {
            transition-delay:2.21s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(14) {
            transition-delay:2.78s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(14) {
            transition-delay:2.33s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(15) {
            transition-delay:2.9s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(15) {
            transition-delay:2.45s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(16) {
            transition-delay:3.02s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(16) {
            transition-delay:2.57s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(17) {
            transition-delay:3.14s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(17) {
            transition-delay:2.69s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(18) {
            transition-delay:3.26s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(18) {
            transition-delay:2.81s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(19) {
            transition-delay:3.38s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(19) {
            transition-delay:2.93s
        }
    }

    @media(min-width: 993px) {
        .active .Jobs-listItem:nth-child(20) {
            transition-delay:3.5s
        }
    }

    @media(max-width: 992px) {
        .active .Jobs-listItem:nth-child(20) {
            transition-delay:3.05s
        }
    }

    .active .Jobs-listItem,.complete .Jobs-listItem {
        opacity: 1;
        transform: translateY(0)
    }

    .Meet-list {
        display: grid;
        position: relative
    }

    @media(min-width: 993px) {
        .Meet-list {
            grid-auto-rows:50%
        }
    }

    @media(max-width: 992px) {
        .Meet-list {
            grid-auto-rows:40vw
        }
    }

    @media(min-width: 577px) {
        .Meet-list {
            grid-template-columns:repeat(2,50%)
        }
    }

    @media(max-width: 576px) {
        .Meet-list {
            grid-auto-rows:70vw
        }
    }

    .Meet-list.is-inactive {
        pointer-events: none
    }

    .Meet-card {
        background-position: 50%;
        background-repeat: no-repeat;
        background-size: cover;
        cursor: pointer;
        overflow: hidden;
        position: relative
    }

    @media(min-width: 993px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(0) {
            transition-delay:.95s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(0) {
            transition-delay:.35s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:first-child .Meet-cardWording>:first-child {
            transition-delay:1.25s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:first-child .Meet-cardWording>:first-child {
            transition-delay:.65s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(2) {
            transition-delay:1.55s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(2) {
            transition-delay:.95s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(3) {
            transition-delay:1.85s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:first-child .Meet-cardWording>:nth-child(3) {
            transition-delay:1.25s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(0) {
            transition-delay:1.1s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(0) {
            transition-delay:.5s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:first-child {
            transition-delay:1.4s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:first-child {
            transition-delay:.8s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.7s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.1s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(3) {
            transition-delay:2s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(2) .Meet-cardWording>:nth-child(3) {
            transition-delay:1.4s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(0) {
            transition-delay:1.25s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(0) {
            transition-delay:.65s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:first-child {
            transition-delay:1.55s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:first-child {
            transition-delay:.95s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.85s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.25s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(3) {
            transition-delay:2.15s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(3) .Meet-cardWording>:nth-child(3) {
            transition-delay:1.55s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(0) {
            transition-delay:1.4s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(0) {
            transition-delay:.8s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:first-child {
            transition-delay:1.7s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:first-child {
            transition-delay:1.1s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(2) {
            transition-delay:2s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.4s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(3) {
            transition-delay:2.3s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(4) .Meet-cardWording>:nth-child(3) {
            transition-delay:1.7s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(0) {
            transition-delay:1.55s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(0) {
            transition-delay:.95s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:first-child {
            transition-delay:1.85s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:first-child {
            transition-delay:1.25s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(2) {
            transition-delay:2.15s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(2) {
            transition-delay:1.55s
        }
    }

    @media(min-width: 993px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(3) {
            transition-delay:2.45s
        }
    }

    @media(max-width: 992px) {
        .active .Meet-card:nth-child(5) .Meet-cardWording>:nth-child(3) {
            transition-delay:1.85s
        }
    }

    @media(max-width: 1440px) {
        .Meet-cardImage {
            position:absolute
        }
    }

    .Meet-cardWording {
        align-content: flex-end;
        align-items: flex-end;
        background: linear-gradient(transparent,rgba(209, 206, 206, 0.3));
        bottom: 0;
        color: #111;
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 1fr max-content;
        height: 50%;
        left: 0;
        padding: 0 30px 1.5625rem;
        pointer-events: none;
        position: absolute;
        right: 0
    }

    @media(max-width: 1440px) {
        .Meet-cardWording {
            padding-bottom:1.5625rem
        }
    }

    .Meet-cardWording>* {
        transform: translateY(300%);
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1);
        will-change: transform
    }

    .active .Meet-cardWording>*,.complete .Meet-cardWording>* {
        transform: translateY(0)
    }

    .Meet-cardPlayIcon {
        grid-row: span 2
    }

    .Meet-cardJobTitle {
        font-size: 1rem;
        padding-bottom: .25rem
    }

    @media(max-width: 1440px) {
        .Meet-cardJobTitle {
            font-size:.875rem
        }
    }

    .Meet-cardQuotation {
        font-size: .75rem
    }

    @media(max-width: 1440px) {
        .Meet-cardQuotation {
            font-size:.625rem
        }
    }

    .Process-inner {
        padding-bottom: 6vh;
        padding-top: 6vh
    }

    @media(max-width: 992px) {
        .Process-inner {
            padding-left:7.6vw;
            padding-right: 7.6vw
        }
    }

    .Process-subhead {
        font-weight: 800
    }

    @media(min-width: 1441px) {
        .Process-subhead {
            font-size:.875rem
        }
    }

    .Process-text {
        margin: 0 auto;
        max-width: 660px;
        padding: 0;
        text-align: center
    }

    @media(max-width: 1440px) {
        .Process-text {
            max-width:520px
        }
    }

    .Process-paragraph {
        font-weight: 300
    }

    .Process-list {
        display: flex;
        justify-content: center;
        padding: 7vh 1.3vw 0
    }

    @media(max-width: 576px) {
        .Process-list {
            padding-left:0;
            padding-right: 0
        }
    }

    @media(max-width: 992px) {
        .Process-list {
            align-items:center;
            flex-direction: column
        }
    }

    .Process-listItem {
        counter-increment: process-number;
        flex: 1;
        max-width: calc(220px + 2.6vw);
        opacity: 1;;
        padding: 0 1.3vw;
        transform: translateY(120px);
        transition: opacity .3s linear,transform 1s cubic-bezier(.165,.84,.44,1);
        will-change: opacity,transform
    }

    @media(max-width: 992px) {
        .Process-listItem {
            max-width:calc(450px + 2.6vw)
        }
    }

    .active .Process-listItem,.complete .Process-listItem {
        opacity: 1;
        transform: translateY(0)
    }

    @media(min-width: 993px) {
        .Process-listItem:nth-child(0) {
            transition-delay:1.45s
        }

        .is-safari .Process-listItem:nth-child(0) {
            transition-delay: .45s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:nth-child(0) {
            transition-delay:1s
        }
    }

    @media(min-width: 993px) {
        .Process-listItem:first-child {
            transition-delay:1.57s
        }

        .is-safari .Process-listItem:first-child {
            transition-delay: .57s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:first-child {
            transition-delay:1.12s
        }
    }

    @media(min-width: 993px) {
        .Process-listItem:nth-child(2) {
            transition-delay:1.69s
        }

        .is-safari .Process-listItem:nth-child(2) {
            transition-delay: .69s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:nth-child(2) {
            transition-delay:1.24s
        }
    }

    @media(min-width: 993px) {
        .Process-listItem:nth-child(3) {
            transition-delay:1.81s
        }

        .is-safari .Process-listItem:nth-child(3) {
            transition-delay: .81s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:nth-child(3) {
            transition-delay:1.36s
        }
    }

    @media(min-width: 993px) {
        .Process-listItem:nth-child(4) {
            transition-delay:1.93s
        }

        .is-safari .Process-listItem:nth-child(4) {
            transition-delay: .93s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:nth-child(4) {
            transition-delay:1.48s
        }
    }

    @media(min-width: 993px) {
        .Process-listItem:nth-child(5) {
            transition-delay:2.05s
        }

        .is-safari .Process-listItem:nth-child(5) {
            transition-delay: 1.05s
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:nth-child(5) {
            transition-delay:1.6s
        }
    }

    .Process-listItem:before {
        content: "0" counter(process-number);
        display: block;
        font-size: 6.25rem;
        font-weight: 200;
        letter-spacing: -2px;
        line-height: 1;
        margin-bottom: .3125rem;
        margin-left: -10px;
        opacity: .08
    }

    @media(max-width: 1440px) {
        .Process-listItem:before {
            font-size:80px
        }
    }

    @media(max-width: 992px) {
        .Process-listItem:before {
            margin-bottom:-55px
        }
    }

    @media(min-width: 1441px) {
        .Process-listItemTitle {
            font-size:1.5rem
        }
    }

    @media(max-width: 1440px) {
        .Process-listItemTitle {
            font-size:1.375rem
        }
    }

    @media(max-width: 992px) {
        .Process-listItemTitle {
            padding-left:60px
        }
    }

    @media(max-width: 576px) {
        .Process-listItemTitle {
            padding-left:20px
        }
    }

    .Process-listItemParagraph {
        opacity: .6
    }

    @media(max-width: 992px) {
        .Process-listItemParagraph {
            padding-left:60px
        }
    }

    @media(max-width: 576px) {
        .Process-listItemParagraph {
            padding-left:20px
        }
    }

    @media(max-width: 992px) {
        .Comfort {
            display:flex;
            flex-direction: column;
            padding-top: 50px
        }

        .Comfort-text {
            order: -1
        }

        .Comfort-video {
            display: flex;
            flex-direction: column;
            overflow: visible;
            overflow: initial;
            width: 100%
        }

        .Comfort-video video {
            position: static
        }

        .Comfort-mobileMask {
            padding-left: 8.6vw
        }

        .Comfort-mobileMask:before {
            left: 0
        }

        .complete .Comfort-mobileMask:before {
            width: 9.6vw
        }
    }

    .Comfort-stats {
        bottom: 35px
    }

    .Comfort-stats:after {
        display: none
    }

    @media(max-width: 992px) {
        .Cost {
            padding-top:50px
        }

        .Cost-text {
            order: -1
        }

        .Cost-image {
            display: flex;
            flex-direction: column
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Cost-stats {
            padding-top:50px
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .Cost-statsItem {
            margin:0 10px
        }

        .Cost-statsItem:before {
            display: none
        }

        .Cost-statsItem span {
            width: 150px
        }
    }

    @media(max-width: 992px) {
        .Safety .fp-tableCell {
            display:flex;
            flex-direction: column
        }
    }

    @media(max-width: 576px) {
        .Safety {
            padding-top:50px
        }
    }

    @media(max-width: 992px) {
        .Safety-title {
            margin-right:9vw;
            min-width: 250px
        }
    }

    .Safety-videos {
        display: flex;
        position: relative;
        z-index: 1
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Safety-videos {
            height:50vw
        }
    }

    @media(max-width: 576px) {
        .Safety-videos {
            background:#0b2819;
            flex-direction: column;
            padding: 30px 8.6vw 20px
        }
    }

    .Safety-videos:after {
        background-color: rgba(17,18,17,.5);
        bottom: 0;
        content: "";
        display: block;
        left: 0;
        opacity: 1;
        opacity: 0;
        position: absolute;
        right: 0;
        top: 0;
        transition: opacity .2s linear;
        will-change: opacity;
        z-index: 1
    }

    .Safety-videos.is-finished:after {
        opacity: 1
    }

    @media(max-width: 576px) {
        .Safety-text {
            order:-1
        }
    }

    .Safety-video {
        height: 100%;
        overflow: hidden;
        position: relative;
        width: 50%
    }

    @media(max-width: 576px) {
        .Safety-video {
            margin-bottom:30px;
            opacity: 1;
            transition: opacity .2s linear .4s;
            width: auto;
            will-change: opacity
        }

        .complete .Safety-video {
            opacity: 1
        }
    }

    .Safety-videoLabel {
        align-items: center;
        background-color: #0b2819;
        bottom: 0;
        color: #fff;
        display: block;
        display: flex;
        font-size: .625rem;
        font-weight: 800;
        height: 30px;
        justify-content: center;
        letter-spacing: 1px;
        position: absolute;
        text-transform: uppercase;
        width: 100%;
        z-index: 1
    }

    @media(max-width: 576px) {
        .Safety-videoLabel {
            height:auto;
            justify-content: flex-start;
            padding-top: 10px;
            position: static
        }
    }

    .Safety-videoLabel--important {
        color: #1efd8d
    }

    .Safety-replay {
        align-items: center;
        background-color: #fff;
        border-radius: 100px;
        color: #0b2819;
        cursor: pointer;
        display: flex;
        font-size: 13px;
        font-weight: 300;
        left: 50%;
        letter-spacing: 1px;
        padding: 8px 15px;
        position: absolute;
        top: 50%;
        transform: translate(-50%,-50%);
        z-index: 2
    }

    @media(max-width: 576px) {
        .Safety-replay {
            font-size:.625rem
        }
    }

    .Safety-replay:hover .Safety-replayIcon {
        transform: rotate(-180deg)
    }

    .Safety-replay.v-enter-active,.Safety-replay.v-leave-active {
        transition: opacity .2s linear;
        will-change: opacity
    }

    .Safety-replay.v-enter-active {
        transition-delay: .15s
    }

    .Safety-replay.v-enter,.Safety-replay.v-leave-to {
        opacity: 1;
    }

    .Safety-replayIcon {
        margin-right: 8px;
        transform: rotate(0);
        transform-origin: 9px 7px;
        transition: transform .6s cubic-bezier(.77,0,.175,1);
        will-change: transform
    }

    @media(max-width: 576px) {
        .Safety-replayIcon {
            transform:scale(.9)
        }
    }

    .Safety-pressure {
        bottom: 60px;
        color: #fff;
        font-size: 2.25rem;
        font-weight: 400;
        left: 50%;
        position: absolute;
        transform: translateX(-50%);
        transition: opacity .2s linear;
        will-change: opacity
    }

    @media(max-width: 576px) {
        .Safety-pressure {
            bottom:25px;
            left: 10px;
            transform: none
        }
    }

    .complete .Safety-pressure {
        opacity: 1
    }

    .Safety-pressureNumber {
        display: inline-block;
        text-align: right;
        width: 70px
    }

    @media(max-width: 576px) {
        .Safety-pressureNumber {
            font-size:1.4375rem;
            width: 36px
        }
    }

    .Safety-pressureUnit {
        font-size: 24px;
        margin-left: 10px
    }

    @media(max-width: 576px) {
        .Safety-pressureUnit {
            font-size:.8125rem
        }
    }

    @media(max-width: 992px) {
        .Speed {
            padding-bottom:50px;
            padding-top: 50px
        }
    }

    .Stats {
        bottom: 7vh;
        color: #fff;
        display: flex;
        justify-content: center;
        left: 50%;
        position: absolute;
        transform: translateX(-50%)
    }

    @media(max-width: 992px) {
        .Stats {
            color:inherit;
            margin: 0 auto;
            padding-bottom: 50px;
            padding-top: 30px;
            position: static;
            transform: none
        }
    }

    @media(max-width: 576px) {
        .Stats {
            padding:30px 0
        }
    }

    @media(min-width: 993px) {
        .Stats:after {
            background:radial-gradient(ellipse at center,rgba(0,0,0,.2) 30%,transparent 70%);
            bottom: -90%;
            content: "";
            display: block;
            left: -50%;
            position: absolute;
            right: -50%;
            top: -90%;
            z-index: -1
        }
    }

    .Stats-item {
        align-items: center;
        display: flex;
        font-size: 10px;
        font-weight: 800;
        letter-spacing: 1px;
        text-align: center;
        text-transform: uppercase
    }

    @media(max-width: 576px) {
        .Stats-item {
            align-items:flex-start;
            font-size: .5rem
        }
    }

    .Stats-item:not(:first-child):before {
        content: "";
        width: 1px
    }

    @media(min-width: 993px) {
        .Stats-item:not(:first-child):before {
            background:#fff;
            height: 56px;
            margin: 0 25px
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Stats-item:not(:first-child):before {
            background:#111;
            height: 70px;
            margin: 0 35px
        }
    }

    @media(max-width: 576px) {
        .Stats-item:not(:first-child):before {
            background:#111;
            height: 56px;
            margin: 0 10px
        }
    }

    @media(min-width: 993px) {
        .Stats-item span {
            width:190px
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Stats-item span {
            width:120px
        }
    }

    @media(max-width: 576px) {
        .Stats-item span {
            width:90px
        }
    }

    .Stats-item strong {
        display: block;
        font-size: 2rem;
        font-weight: 200
    }

    @media(min-height: 577px)and (max-width:1440px) {
        .Stats-item strong {
            font-size:1.5rem;
            margin-bottom: 5px
        }
    }

    @media(max-width: 576px) {
        .Stats-item strong {
            font-size:1rem;
            margin-bottom: 10px
        }
    }

    @media(max-width: 992px) {
        .Sustainability {
            padding:50px 0
        }

        .Sustainability .fp-tableCell {
            display: flex;
            flex-direction: column
        }

        .Sustainability-text {
            order: -1
        }
    }

    .NewsHomeSidebar {
        position: relative;
        z-index: 200
    }

    .NewsHomeSidebar.v-enter-active,.NewsHomeSidebar.v-leave-active {
        transition: transform 1s cubic-bezier(.86,0,.07,1)
    }

    .NewsHomeSidebar-inner {
        background-color: #fff;
        bottom: 0;
        overflow: scroll;
        position: fixed;
        right: 0;
        top: 0;
        z-index: 20
    }

    @media(min-width: 993px) {
        @-moz-document url-prefix() {
            .NewsHomeSidebar-inner {
                scrollbar-width:none
            }
        }

        .NewsHomeSidebar-inner::-webkit-scrollbar {
            display: none;
            scrollbar-width: none
        }
    }

    @media(min-width: 769px) {
        .NewsHomeSidebar-inner {
            width:75vw
        }
    }

    .NewsHomeSidebar.v-enter-active .NewsHomeSidebar-inner,.NewsHomeSidebar.v-leave-active .NewsHomeSidebar-inner {
        transition: transform 1s cubic-bezier(.86,0,.07,1)
    }

    .NewsHomeSidebar.v-enter .NewsHomeSidebar-inner,.NewsHomeSidebar.v-leave-to .NewsHomeSidebar-inner {
        transform: translateX(100%)
    }

    .NewsHomeSidebar-backdrop {
        -webkit-backdrop-filter: blur(5px);
        backdrop-filter: blur(5px);
        background-color: hsla(0,0%,7%,.5);
        bottom: 0;
        left: 0;
        opacity: 1;
        position: fixed;
        right: 0;
        top: 0;
        z-index: 19
    }

    .NewsHomeSidebar.v-enter-active .NewsHomeSidebar-backdrop,.NewsHomeSidebar.v-leave-active .NewsHomeSidebar-backdrop {
        transition: opacity .2s linear .3s
    }

    .NewsHomeSidebar.v-enter .NewsHomeSidebar-backdrop,.NewsHomeSidebar.v-leave-to .NewsHomeSidebar-backdrop {
        opacity: 1;
    }

    .NewsHomeSidebar-wys {
        padding: 14% 13.8vw 16%
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-wys {
            padding-left:8.6vw;
            padding-right: 8.6vw
        }
    }

    .NewsHomeSidebar-wys h2,.NewsHomeSidebar-wys h3,.NewsHomeSidebar-wys h4,.NewsHomeSidebar-wys h5 {
        margin-bottom: 1.5em
    }

    .NewsHomeSidebar-wys p {
        font-weight: 100;
        margin-bottom: 1.5em
    }

    .NewsHomeSidebar-blockquote {
        padding: 14% 13.8vw 16%
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-blockquote {
            padding-left:8.6vw;
            padding-right: 8.6vw
        }
    }

    .NewsHomeSidebar-blockquoteQuotation:before {
        content: "« ";
        display: inline
    }

    .NewsHomeSidebar-blockquoteQuotation:after {
        content: " »";
        display: inline
    }

    .NewsHomeSidebar-blockquoteAuthor {
        grid-column-gap: 15px;
        align-items: center;
        -moz-column-gap: 15px;
        column-gap: 15px;
        display: grid;
        font-weight: 300;
        grid-auto-rows: max-content;
        grid-template-columns: max-content 1fr;
        padding-top: 50px
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-blockquoteAuthor {
            padding-top:30px
        }
    }

    .NewsHomeSidebar-blockquoteAuthorAvatar {
        border-radius: 100%;
        grid-row: span 2;
        height: 50px;
        overflow: hidden;
        position: relative;
        width: 50px
    }

    .NewsHomeSidebar-blockquoteAuthorName {
        letter-spacing: -.02em;
        padding-top: 4px
    }

    .NewsHomeSidebar-blockquoteAuthorJobTitle {
        font-size: .875rem;
        letter-spacing: -.02em;
        opacity: .4;
        padding-bottom: 4px
    }

    .NewsHomeSidebar-link,.NewsHomeSidebar-share {
        align-items: center;
        cursor: pointer;
        display: flex;
        font-weight: 100;
        justify-content: space-between;
        padding-left: 60px;
        padding-right: 60px
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-link,.NewsHomeSidebar-share {
            font-size:1rem;
            padding-left: 8.6vw;
            padding-right: 8.6vw
        }
    }

    .NewsHomeSidebar-link {
        background-color: #111;
        color: #fff;
        height: 12.5vw;
        margin-top: 10%;
        max-height: 200px
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-link {
            height:24vw
        }

        .NewsHomeSidebar-linkIcon {
            width: 18px
        }
    }

    .NewsHomeSidebar-share {
        color: #111;
        height: 8.75vw;
        max-height: 140px
    }

    @media(max-width: 576px) {
        .NewsHomeSidebar-share {
            height:20vw
        }

        .NewsHomeSidebar-shareIcon {
            width: 18px
        }
    }

    .NewsHomeSidebar-clipboard {
        grid-gap: 5px;
        align-items: center;
        background-color: #111;
        border-radius: 3px;
        bottom: 10%;
        color: #fff;
        display: grid;
        grid-auto-flow: column;
        left: 50%;
        opacity: 1;
        padding: 5px 10px;
        pointer-events: none;
        position: absolute;
        transform: translateX(-50%);
        transition: opacity .5s linear
    }

    .NewsHomeSidebar-clipboard.is-active {
        opacity: 1
    }

    .NewsHomeSidebar-backButton {
        color: #111;
        cursor: pointer;
        left: 15px;
        position: fixed;
        top: 15px;
        transform: scaleX(-1);
        z-index: 99999
    }

    @media screen and (min-width: 769px) {
        .NewsHomeSidebar-backButton {
            display:none
        }
    }

    @media(max-width: 992px) {
        .Technology .fp-tableCell {
            flex-direction:row
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Technology .fp-tableCell {
            min-height:600px
        }
    }

    @media(max-width: 576px) {
        .Technology .fp-tableCell {
            flex-direction:column
        }
    }

    @media(min-width: 993px) {
        .Technology-text {
            padding-top:12vh!important
        }
    }

    @media(min-width: 1441px) {
        .Technology-timer {
            margin-bottom:3.125rem
        }
    }

    @media(max-width: 1440px) {
        .Technology-timer {
            margin-bottom:1.875rem
        }
    }

    .Technology-timerList {
        margin-bottom: 45px;
        position: relative
    }

    .Technology-timerListItem {
        color: #0b2819;
        display: block;
        height: 20px;
        overflow: hidden;
        position: absolute;
        width: 100%
    }

    .Technology-timerListItem span {
        position: absolute
    }

    .Technology-timerListItem .timer.v-enter-active,.Technology-timerListItem .timer.v-leave-active {
        transition: transform 1.4s cubic-bezier(.86,0,.07,1);
        will-change: transform
    }

    .Technology-timerListItem .timer.v-enter {
        transform: translateY(-100%)
    }

    .Technology-timerListItem .timer.v-leave-to {
        transform: translateY(100%)
    }

    .Technology-timerListItem .timer.v-enter-to,.Technology-timerListItem .timer.v-leave {
        transform: translateY(0)
    }

    .Technology-timerLines {
        display: flex
    }

    .Technology-timerLinesItem {
        background-color: rgba(11,40,25,.2);
        height: 1px;
        position: relative;
        width: 90px
    }

    .Technology-timerLinesItem:before {
        background-color: #0b2819;
        content: "";
        display: block;
        height: 100%;
        position: absolute;
        width: 0;
        will-change: width
    }

    .Technology-timerLinesItem.is-active:before {
        transition: width var(--delai) linear,opacity 0s linear;
        width: 100%
    }

    .Technology-timerLinesItem.is-finished:before {
        width: 100%
    }

    .Technology-timerLinesItem:not(:first-child) {
        margin-left: 10px
    }

    .ProjectCard {
        background-color: #111;
        cursor: pointer;
        overflow: hidden;
        padding-bottom: 56.25%;
        position: relative;
        transition: transform 1s cubic-bezier(.77,0,.175,1);
        width: 100%
    }

    .ProjectCard:hover .Project-heroMedia,.ProjectCard:hover .ProjectCard-media {
        transform: scale(1.03)
    }

    .Project-heroMedia,.ProjectCard-media {
        bottom: 0;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        transition: opacity .3s linear,transform 1.2s cubic-bezier(.23,1,.32,1)
    }

    .Project-heroMedia:after,.ProjectCard-media:after {
        background-image: linear-gradient(180deg,transparent,rgba(0,0,0,.6));
        bottom: 0;
        content: "";
        height: 50%;
        left: 0;
        position: absolute;
        width: 100%
    }

    .Project-heroContent,.ProjectCard-content {
        grid-gap: 10px;
        align-content: flex-end;
        bottom: 0;
        color: #fff;
        display: grid;
        gap: 10px;
        height: 50%;
        left: 0;
        pointer-events: none;
        position: absolute;
        right: 0
    }

    @media(min-width: 1201px) {
        .Project-heroContent,.ProjectCard-content {
            padding:30px
        }
    }

    @media(max-width: 1200px) {
        .Project-heroContent,.ProjectCard-content {
            padding:20px
        }
    }

    .Project-heroInfos,.ProjectCard-infos {
        align-items: center;
        display: flex;
        flex-wrap: wrap;
        gap: 4px
    }

    .ProjectCard-name {
        font-size: 3.125rem;
        letter-spacing: -.02em
    }

    @media(max-width: 1440px) {
        .ProjectCard-name {
            font-size:2rem
        }
    }

    .Project-heroSurfaceArea,.ProjectCard-surfaceArea {
        font-size: .875rem
    }

    .ProjectCTACard {
        background-color: #0b2819
    }

    .ProjectCTACard:hover .ProjectCTACard-link {
        background-position: 0 100%;
        background-size: 100% .05em;
        transition-timing-function: cubic-bezier(.165,.84,.44,1)
    }

    .ProjectCTACard-content {
        align-items: flex-end;
        color: #1efd8d;
        display: flex;
        justify-content: space-between;
        padding: 160px 100px 120px;
        pointer-events: none
    }

    @media(max-width: 1440px) {
        .ProjectCTACard-content {
            padding:100px 80px 90px
        }
    }

    @media(max-width: 1200px) {
        .ProjectCTACard-content {
            font-size:3.75rem;
            padding: 70px 50px 60px
        }
    }

    @media(max-width: 992px) {
        .ProjectCTACard-content {
            font-size:2.75rem;
            padding: 50px 40px
        }
    }

    @media(max-width: 576px) {
        .ProjectCTACard-content {
            font-size:1.875rem;
            padding: 40px 20px 30px
        }
    }

    .ProjectCTACard-link {
        background: linear-gradient(90deg,currentColor 72%,#1efd8d 0) 100% 100% no-repeat;
        background-size: 0 .05em;
        color: #fff;
        font-size: 6.875rem;
        letter-spacing: -.012em;
        line-height: 1;
        -webkit-text-decoration: none;
        text-decoration: none;
        transition: background-size .5s cubic-bezier(.895,.03,.685,.22)
    }

    @media(max-width: 1440px) {
        .ProjectCTACard-link {
            font-size:5rem
        }
    }

    @media(max-width: 1200px) {
        .ProjectCTACard-link {
            font-size:3.75rem
        }
    }

    @media(max-width: 992px) {
        .ProjectCTACard-link {
            font-size:2.75rem
        }
    }

    @media(max-width: 576px) {
        .ProjectCTACard-link {
            font-size:1.875rem
        }
    }

    .ProjectCTACard-icon {
        margin-bottom: 15px
    }

    @media(max-width: 1440px) {
        .ProjectCTACard-icon {
            height:4vw;
            margin-bottom: 1.2vw;
            width: 4vw
        }
    }

    .ProjectsCarousel {
        align-items: center;
        display: flex;
        gap: 50px;
        justify-content: center;
        padding-top: 5vw;
        position: relative
    }

    .ProjectsCarousel.v-leave-active {
        transition: opacity .5s linear,transform .5s cubic-bezier(.895,.03,.685,.22)
    }

    .ProjectsCarousel.v-leave-active .ProjectsCarousel-navigation {
        transition: opacity .5s linear
    }

    .ProjectsCarousel.v-enter-active {
        position: fixed;
        top: 50%;
        transform: translateY(-50%);
        transition: pointer-events 2s linear
    }

    .ProjectsCarousel.v-enter-active .ProjectsCarousel-navigation {
        transition: opacity .4s linear 1.1s
    }

    .ProjectsCarousel.v-enter .ProjectsCarousel-navigation,.ProjectsCarousel.v-leave-to .ProjectsCarousel-navigation {
        opacity: 1;
    }

    .ProjectsCarousel.v-leave-to {
        opacity: 1;
        transform: scale(.85)
    }

    .ProjectsCarousel-list {
        align-items: center;
        display: flex;
        justify-content: center;
        position: relative;
        z-index: 1
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-list {
            max-width:70vw;
            width: 135vmin
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-list {
            width:120vmin
        }
    }

    .ProjectsCarousel-list .ProjectCTACard-content {
        bottom: 0;
        left: 0;
        position: absolute;
        right: 0;
        top: 0
    }

    .ProjectsCarousel-list .ProjectCard-media {
        background-color: #2b2b2b;
        opacity: 1;
        transition: none
    }

    .ProjectsCarousel-list .ProjectCard-media img.is-lazy,.ProjectsCarousel-list .ProjectCard-media video.is-lazy {
        transition-delay: .7s
    }

    .ProjectsCarousel-listItem {
        opacity: 1;
        perspective: 3000px;
        position: absolute;
        transform: translateY(calc(-24% - 120px + 6vw)) scale(.82);
        transition: none;
        width: 100%
    }

    .ProjectsCarousel-listItem[data-position="0"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 6
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="0"] {
            transform:translateY(0) scale(1)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="0"] {
            transform:translateY(0) scale(1)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="0"] {
            transform:translateY(0) scale(1)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="0"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="0"] .ProjectCard-media {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="1"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 5
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="1"] {
            transform:translateY(calc(-4% - 20px + 1vw)) scale(.97)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="1"] {
            transform:translateY(-4%) scale(.97)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="1"] {
            transform:translateY(calc(-4% - 20px + 1vw)) scale(.97)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="1"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="1"] .ProjectCard-media {
        opacity: .8333333333;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="2"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 4
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="2"] {
            transform:translateY(calc(-8% - 40px + 2vw)) scale(.94)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="2"] {
            transform:translateY(-8%) scale(.94)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="2"] {
            transform:translateY(calc(-8% - 40px + 2vw)) scale(.94)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="2"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="2"] .ProjectCard-media {
        opacity: .6666666667;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="3"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 3
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="3"] {
            transform:translateY(calc(-12% - 60px + 3vw)) scale(.91)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="3"] {
            transform:translateY(-12%) scale(.91)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="3"] {
            transform:translateY(calc(-12% - 60px + 3vw)) scale(.91)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="3"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="3"] .ProjectCard-media {
        opacity: .5;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="4"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 2
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="4"] {
            transform:translateY(calc(-16% - 80px + 4vw)) scale(.88)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="4"] {
            transform:translateY(-16%) scale(.88)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="4"] {
            transform:translateY(calc(-16% - 80px + 4vw)) scale(.88)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="4"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="4"] .ProjectCard-media {
        opacity: .3333333333;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="5"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 1
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="5"] {
            transform:translateY(calc(-20% - 100px + 5vw)) scale(.85)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="5"] {
            transform:translateY(-20%) scale(.85)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="5"] {
            transform:translateY(calc(-20% - 100px + 5vw)) scale(.85)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="5"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="5"] .ProjectCard-media {
        opacity: .1666666667;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem[data-position="6"] {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1);
        z-index: 0
    }

    @media(min-width: 1441px) {
        .ProjectsCarousel-listItem[data-position="6"] {
            transform:translateY(calc(-24% - 120px + 6vw)) scale(.82)
        }
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-listItem[data-position="6"] {
            transform:translateY(-24%) scale(.82)
        }
    }

    @media(max-width: 992px) {
        .ProjectsCarousel-listItem[data-position="6"] {
            transform:translateY(calc(-24% - 120px + 6vw)) scale(.82)
        }
    }

    @media(max-width: 767px) {
        .ProjectsCarousel-listItem[data-position="6"] {
            transform:none
        }
    }

    .ProjectsCarousel-listItem[data-position="6"] .ProjectCard-media {
        opacity: 1;
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .3s linear
    }

    .ProjectsCarousel-listItem:not([data-position="0"]) {
        pointer-events: none
    }

    .ProjectsCarousel-listItem.from-bottom,.ProjectsCarousel-listItem.to-bottom {
        opacity: 1;
        z-index: 7
    }

    .ProjectsCarousel-listItem.from-bottom {
        transform: translateY(200%) scale(1.8);
        transition: none
    }

    .ProjectsCarousel-listItem.from-bottom .ProjectCard-media {
        opacity: 1;
        transform: scale(1.8);
        transition: none
    }

    .ProjectsCarousel-listItem.to-bottom {
        transform: translateY(200%) scale(1)
    }

    .ProjectsCarousel-listItem.to-bottom,.ProjectsCarousel-listItem.to-bottom .ProjectCard-media {
        transition: transform 1.2s cubic-bezier(.23,1,.32,1),opacity .5s linear .8s
    }

    .ProjectsCarousel-navigation {
        grid-gap: 5px;
        color: hsla(0,0%,100%,.3);
        display: grid;
        gap: 5px
    }

    @media(max-width: 1440px) {
        .ProjectsCarousel-navigation {
            display:none
        }
    }

    .ProjectsCarousel-navigationArrow {
        align-items: center;
        background-color: #1b1b1b;
        border-radius: 100%;
        cursor: pointer;
        display: flex;
        height: 60px;
        justify-content: center;
        transition: background-color .3s linear,color .3s linear;
        width: 60px
    }

    .ProjectsCarousel-navigationArrow:hover {
        background-color: #252525;
        color: #1efd8d;
        transition-duration: 0s
    }

    .ProjectsCarousel-navigationArrow--down {
        transform: scaleY(-1)
    }

    .ProjectsGrid.v-enter .ProjectsGrid-rows {
        opacity: 1;
        transform: scale(.5);
        transform-origin: top
    }

    .ProjectsGrid.v-enter .ProjectsGrid-row {
        transform: translateY(100vh)
    }

    .ProjectsGrid.v-enter .ProjectsGrid-filters {
        transform: translateY(100%)
    }

    .ProjectsGrid.v-enter-active {
        transition: pointer-events 2s linear
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-rows {
        transition: opacity .5s linear,transform 1.4s cubic-bezier(.23,1,.32,1)
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row {
        transition: transform 1.4s cubic-bezier(.23,1,.32,1)
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:first-child {
        transition-delay: 0s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(2) {
        transition-delay: .12s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(3) {
        transition-delay: .24s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(4) {
        transition-delay: .36s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(5) {
        transition-delay: .48s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(6) {
        transition-delay: .6s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(7) {
        transition-delay: .72s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(8) {
        transition-delay: .84s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(9) {
        transition-delay: .96s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-row:nth-child(10) {
        transition-delay: 1.08s
    }

    .ProjectsGrid.v-enter-active .ProjectsGrid-filters {
        transition: transform .7s cubic-bezier(.23,1,.32,1) 1s
    }

    .ProjectsGrid.v-leave-active {
        transition: pointer-events 2s linear
    }

    .ProjectsGrid.v-leave-active .ProjectsGrid-rows {
        transition: opacity .5s linear,transform .5s cubic-bezier(.895,.03,.685,.22)
    }

    .ProjectsGrid.v-leave-active .ProjectsGrid-filters {
        transition: transform .7s cubic-bezier(.86,0,.07,1) .6s
    }

    .ProjectsGrid.v-leave-to .ProjectsGrid-rows {
        opacity: 1;
        transform: scale(.95);
        transform-origin: top
    }

    .ProjectsGrid.v-leave-to .ProjectsGrid-filters {
        transform: translateY(100%)
    }

    @media(min-width: 1201px) {
        .ProjectsGrid-row[data-row-type="1-card-100"] .ProjectCard {
            height:750px;
            padding: 0
        }
    }

    .ProjectsGrid-row[data-row-type="2-cards-50-50"] {
        grid-gap: 10px;
        display: grid;
        gap: 10px
    }

    @media(min-width: 577px) {
        .ProjectsGrid-row[data-row-type="2-cards-50-50"] {
            grid-template-columns:repeat(2,1fr)
        }
    }

    .ProjectsGrid-row[data-row-type="3-cards-66-33-33"] {
        grid-gap: 10px;
        display: grid;
        gap: 10px
    }

    @media(min-width: 993px) {
        .ProjectsGrid-row[data-row-type="3-cards-66-33-33"] {
            grid-template:repeat(2,max-content)/66.6666666667% 1fr
        }
    }

    @media(max-width: 992px)and (min-width:577px) {
        .ProjectsGrid-row[data-row-type="3-cards-66-33-33"] {
            grid-template:repeat(2,max-content)/repeat(2,1fr)
        }
    }

    @media(min-width: 993px) {
        .ProjectsGrid-row[data-row-type="3-cards-66-33-33"]>:first-child {
            grid-row:span 2
        }
    }

    @media(max-width: 992px)and (min-width:577px) {
        .ProjectsGrid-row[data-row-type="3-cards-66-33-33"]>:first-child {
            grid-column:span 2
        }
    }

    .ProjectsGrid-row[data-row-type="3-cards-33-33-66"] {
        grid-gap: 10px;
        display: grid;
        gap: 10px
    }

    @media(min-width: 993px) {
        .ProjectsGrid-row[data-row-type="3-cards-33-33-66"] {
            grid-template:repeat(2,max-content)/1fr 66.6666666667%
        }
    }

    @media(max-width: 992px)and (min-width:577px) {
        .ProjectsGrid-row[data-row-type="3-cards-33-33-66"] {
            grid-template:repeat(2,max-content)/1fr 66.6666666667%
        }
    }

    @media(max-width: 576px) {
        .ProjectsGrid-row[data-row-type="3-cards-33-33-66"] {
            grid-template:unset
        }
    }

    @media(min-width: 993px) {
        .ProjectsGrid-row[data-row-type="3-cards-33-33-66"]>:last-child {
            grid-row:span 2
        }
    }

    @media(max-width: 992px)and (min-width:577px) {
        .ProjectsGrid-row[data-row-type="3-cards-33-33-66"]>:last-child {
            grid-column:span 2
        }
    }

    .ProjectsGrid-inner {
        max-width: 1920px;
        width: 100vw
    }

    @media(min-width: 577px) {
        .ProjectsGrid-inner {
            padding-bottom:104px;
            padding-top: 104px
        }
    }

    @media(max-width: 576px) {
        .ProjectsGrid-inner {
            padding:80px 0
        }
    }

    .ProjectsGrid-rows {
        grid-gap: 10px;
        display: grid;
        gap: 10px;
        width: 100%
    }

    .ProjectsGrid-rowItem {
        scroll-margin-top: 100px;
        transition: opacity 1s cubic-bezier(.86,0,.07,1),transform 1s cubic-bezier(.86,0,.07,1)
    }

    .ProjectsGrid-rowItem.is-disabled {
        opacity: .3;
        pointer-events: none;
        transform: scale(.98)
    }

    .ProjectsGrid-rowItem.is-higher {
        position: relative;
        z-index: 1
    }

    .ProjectsGrid .ProjectCard {
        padding-bottom: 66.6666666667%
    }

    .ProjectsGrid .ProjectCTACard {
        margin-bottom: 10px;
        padding-bottom: 0
    }

    .ProjectsGrid-filters {
        background-color: #1b1b1b;
        bottom: 0;
        display: flex;
        flex-direction: column;
        height: 420px;
        position: fixed;
        right: 0;
        transform: translateY(calc(100% - 50px));
        transition: transform 1s cubic-bezier(.23,1,.32,1);
        width: 280px
    }

    @media(max-width: 576px) {
        .ProjectsGrid-filters {
            width:100%
        }
    }

    .ProjectsGrid-filters.is-open {
        transform: none
    }

    .ProjectsGrid-filters.is-open .ProjectsGrid-filtersHeaderIcon {
        transform: rotate(45deg)
    }

    .ProjectsGrid-filters.is-open .ProjectsGrid-filtersHeader:hover .ProjectsGrid-filtersHeaderIcon {
        transform: rotate(-45deg)
    }

    .ProjectsGrid-filters:not(.is-open) .ProjectsGrid-filtersHeader:hover .ProjectsGrid-filtersHeaderIcon {
        transform: rotate(90deg)
    }

    .ProjectsGrid-filtersHeader {
        align-items: center;
        color: #fff;
        cursor: pointer;
        display: flex;
        font-size: .625rem;
        font-weight: 500;
        height: 50px;
        justify-content: space-between;
        letter-spacing: -.01em;
        padding: 10px 20px;
        text-transform: uppercase;
        transition: background-color .2s linear
    }

    .ProjectsGrid-filtersHeader:hover {
        background-color: #252525
    }

    .ProjectsGrid-filtersHeaderIcon {
        transition: transform .6s cubic-bezier(.23,1,.32,1)
    }

    .ProjectsGrid-filtersBody {
        padding: 20px
    }

    .ProjectsGrid-filtersSection {
        display: flex;
        flex-wrap: wrap;
        gap: 4px
    }

    .ProjectsGrid-filtersSection:first-child {
        padding-bottom: 20px
    }

    .ProjectsGrid-filtersSection:not(:first-child) {
        border-top: 1px solid hsla(0,0%,100%,.2);
        padding: 20px 0
    }

    .ProjectsGrid-filterSubmit {
        align-items: center;
        background-color: #fff;
        color: hsla(0,0%,7%,.5);
        cursor: pointer;
        display: flex;
        font-size: .625rem;
        font-weight: 500;
        height: 50px;
        justify-content: space-between;
        letter-spacing: -.01em;
        margin-top: auto;
        padding: 10px 20px;
        text-transform: uppercase
    }

    .ProjectsGrid-filterSubmit span {
        position: relative;
        -webkit-text-decoration: none;
        text-decoration: none
    }

    .ProjectsGrid-filterSubmit span:after {
        background-color: #111;
        bottom: -2px;
        content: "";
        height: 1px;
        left: 0;
        position: absolute;
        transform: scaleX(0);
        transform-origin: right;
        transition: transform .5s cubic-bezier(.895,.03,.685,.22);
        width: 100%
    }

    .ProjectsGrid-filterSubmit:hover span:after {
        transform: scaleX(1);
        transform-origin: left;
        transition-timing-function: cubic-bezier(.165,.84,.44,1)
    }

    .ProjectsGrid-filterSubmit.v-enter-active,.ProjectsGrid-filterSubmit.v-leave-active {
        transition: transform .7s cubic-bezier(.23,1,.32,1)
    }

    .ProjectsGrid-filterSubmit.v-enter,.ProjectsGrid-filterSubmit.v-leave-to {
        transform: translateY(100%)
    }

    .ProjectsGrid-filterSubmit strong,.ProjectsGrid-filterSubmitIcon {
        color: #111
    }

    .ProjectTransition {
        opacity: 1;
        overflow: hidden;
        pointer-events: none;
        position: fixed;
        transition: transform 1s cubic-bezier(.86,0,.07,1),opacity .1s linear,height 1s cubic-bezier(.86,0,.07,1);
        z-index: 20
    }

    .ProjectTransition .ProjectCard {
        all: unset
    }

    .ProjectTransition .ProjectCard-media {
        transform: scale(1.03);
        transition: transform .4s linear .4s
    }

    .ProjectTransition .ProjectCard-name {
        display: inline-block;
        overflow: hidden;
        position: relative
    }

    .ProjectTransition .ProjectCard-name>* {
        display: block;
        transition: transform .7s cubic-bezier(.755,.05,.855,.06)
    }

    @media(min-width: 1441px) {
        [class*=page-projects-slug] .ProjectTransition .ProjectCard-name {
            font-size:1.875rem
        }
    }

    .ProjectTransition .ProjectCard-infos>* {
        transition: transform .7s cubic-bezier(.755,.05,.855,.06),opacity .4s cubic-bezier(.755,.05,.855,.06)
    }

    .ProjectTransition.is-visible .ProjectCard-name>* {
        transform: translateY(-100%)
    }

    .ProjectTransition.is-visible .ProjectCard-media {
        transform: none
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:first-child {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .12s,.12s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(2) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .17s,.17s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(3) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .22s,.22s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(4) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .27s,.27s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(5) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .32s,.32s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(6) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .37s,.37s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(7) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .42s,.42s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(8) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .47s,.47s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(9) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .52s,.52s
    }

    .ProjectTransition.is-visible .ProjectCard-infos>:nth-child(10) {
        opacity: 0;
        transform: translateY(-50%);
        transition-delay: .57s,.57s
    }

    .ProjectTag {
        color: #111;
        cursor: pointer;
        font-size: .625rem;
        padding: 5px 8px
    }

    .ProjectTag--forSale {
        background-color: #fff;
        -webkit-clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px));
        clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px))
    }

    @media(hover: none) {
        .ProjectTag--forSale.is-disabled {
            color:#fff;
            position: relative
        }

        .ProjectTag--forSale.is-disabled:after {
            background-color: #1b1b1b;
            bottom: 1px;
            -webkit-clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px));
            clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px));
            content: "";
            left: 1px;
            position: absolute;
            right: 1px;
            top: 1px;
            z-index: -1
        }
    }

    @media(hover: hover) {
        .ProjectTag--forSale.is-disabled:not(:hover) {
            color:#fff;
            position: relative
        }

        .ProjectTag--forSale.is-disabled:not(:hover):after {
            background-color: #1b1b1b;
            bottom: 1px;
            -webkit-clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px));
            clip-path: polygon(0 4px,2.5px 2.5px,4px 0,calc(100% - 4px) 0,calc(100% - 2.5px) 2.5px,100% 4px,100% calc(100% - 4px),calc(100% - 2.5px) calc(100% - 2.5px),calc(100% - 4px) 100%,4px 100%,2.5px calc(100% - 2.5px),0 calc(100% - 4px));
            content: "";
            left: 1px;
            position: absolute;
            right: 1px;
            top: 1px;
            z-index: -1
        }
    }

    .ProjectTag--category {
        background-color: #606060;
        border-radius: 100px;
        color: #fff
    }

    @media(hover: none) {
        .ProjectTag--category.is-disabled {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #606060
        }
    }

    @media(hover: hover) {
        .ProjectTag--category.is-disabled:not(:hover) {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #606060
        }
    }

    .ProjectTag--status {
        border-radius: 2px
    }

    .ProjectTag--status[data-status=completed] {
        background-color: #1efd8d
    }

    @media(hover: none) {
        .ProjectTag--status[data-status=completed].is-disabled {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #1efd8d;
            color: #1efd8d
        }
    }

    @media(hover: hover) {
        .ProjectTag--status[data-status=completed].is-disabled:not(:hover) {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #1efd8d;
            color: #1efd8d
        }
    }

    .ProjectTag--status[data-status=on-going] {
        background-color: #ff9600
    }

    @media(hover: none) {
        .ProjectTag--status[data-status=on-going].is-disabled {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #ff9600;
            color: #ff9600
        }
    }

    @media(hover: hover) {
        .ProjectTag--status[data-status=on-going].is-disabled:not(:hover) {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #ff9600;
            color: #ff9600
        }
    }

    .ProjectTag--status[data-status=case-study] {
        background-color: #ffe200
    }

    @media(hover: none) {
        .ProjectTag--status[data-status=case-study].is-disabled {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #ffe200;
            color: #ffe200
        }
    }

    @media(hover: hover) {
        .ProjectTag--status[data-status=case-study].is-disabled:not(:hover) {
            background-color:transparent;
            box-shadow: inset 0 0 0 1px #ffe200;
            color: #ffe200
        }
    }

    .NewsCard {
        background-color: #262626;
        cursor: pointer;
        position: relative
    }

    @media(max-width: 576px) {
        .NewsCard {
            height:calc(100vh - 104px)!important
        }
    }

    @media(min-width: 993px) {
        .NewsCard--external {
            height:400px
        }
    }

    @media(max-width: 992px) {
        .NewsCard--external {
            height:300px
        }
    }

    @media(min-width: 993px) {
        .NewsCard--internal {
            height:800px
        }
    }

    @media(max-width: 992px) {
        .NewsCard--internal {
            height:600px
        }
    }

    .NewsCard--internal .NewsCard-arrow {
        transform: rotate(45deg)
    }

    .NewsCard-figure:before {
        background-image: linear-gradient(180deg,transparent,rgba(0,0,0,.4));
        bottom: 0;
        content: "";
        height: 50%;
        left: 0;
        position: absolute;
        right: 0;
        top: auto;
        z-index: 1
    }

    .NewsCard-img {
        position: absolute
    }

    .NewsCard-title {
        font-size: 1.875rem;
        letter-spacing: -.0166666667em;
        margin-right: auto
    }

    @media(max-width: 576px) {
        .NewsCard-title {
            font-size:2.25rem;
            letter-spacing: -.025em;
            line-height: 1
        }
    }

    .NewsCard-link {
        align-items: flex-end;
        bottom: 0;
        display: flex;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        z-index: 1
    }

    @media(min-width: 992px) {
        .NewsCard-link {
            padding:16px 30px
        }
    }

    @media(max-width: 991px) {
        .NewsCard-link {
            padding:16px 20px 100px
        }
    }

    .NewsCard-action {
        grid-gap: 30px;
        display: grid;
        gap: 30px;
        grid-auto-flow: column;
        margin-bottom: 4px
    }

    @media(max-width: 1440px) {
        .NewsCard-action {
            position:absolute;
            right: 30px;
            top: 30px
        }
    }

    @media(max-width: 576px) {
        .NewsCard-arrow {
            display:none
        }
    }

    .NewsSidebar {
        color: #111;
        position: relative;
        z-index: 200
    }

    .NewsSidebar.v-enter-active,.NewsSidebar.v-leave-active {
        transition: all 1.2s cubic-bezier(.86,0,.07,1)
    }

    .NewsSidebar.is-updating .NewsSidebar-inner>:not(:first-child) {
        animation: news-content 1s cubic-bezier(.165,.84,.44,1) .2s forwards,fade-in .4s cubic-bezier(.77,0,.175,1) .2s forwards;
        opacity: 1;
    }

    .NewsSidebar-inner {
        background-color: #fff;
        bottom: 0;
        overflow: auto;
        position: fixed!important;
        right: 0;
        top: 0;
        z-index: 20
    }

    @media(min-width: 993px) {
        @-moz-document url-prefix() {
            .NewsSidebar-inner {
                scrollbar-width:none
            }
        }

        .NewsSidebar-inner::-webkit-scrollbar {
            display: none;
            scrollbar-width: none
        }
    }

    @media(min-width: 993px) {
        .NewsSidebar-inner {
            width:75vw
        }
    }

    @media(max-width: 992px) {
        .NewsSidebar-inner {
            width:100vw
        }
    }

    .NewsSidebar.v-enter-active .NewsSidebar-inner,.NewsSidebar.v-leave-active .NewsSidebar-inner {
        transition: transform 1s cubic-bezier(.86,0,.07,1)
    }

    .NewsSidebar.v-enter .NewsSidebar-inner,.NewsSidebar.v-leave-to .NewsSidebar-inner {
        transform: translateX(100%)
    }

    .NewsSidebar-backdrop {
        -webkit-backdrop-filter: blur(5px);
        backdrop-filter: blur(5px);
        background-color: hsla(0,0%,7%,.5);
        bottom: 0;
        left: 0;
        opacity: 1;
        position: fixed;
        right: 0;
        top: 0;
        z-index: 19
    }

    .NewsSidebar.v-enter-active .NewsSidebar-backdrop,.NewsSidebar.v-leave-active .NewsSidebar-backdrop {
        transition: opacity .2s linear .3s
    }

    .NewsSidebar.v-enter .NewsSidebar-backdrop,.NewsSidebar.v-leave-to .NewsSidebar-backdrop {
        opacity: 1;
    }

    @media(max-width: 576px) {
        .NewsSidebar-hero {
            height:var(--hero-height)
        }
    }

    .NewsSidebar-wys {
        box-sizing: content-box;
        margin: 12% auto;
        max-width: 750px;
        padding-left: 8.6vw;
        padding-right: 8.6vw
    }

    @media(max-width: 576px) {
        .NewsSidebar-wys {
            margin:30% auto
        }
    }

    .NewsSidebar-wys h2,.NewsSidebar-wys h3,.NewsSidebar-wys h4,.NewsSidebar-wys h5 {
        margin-bottom: 1.5em
    }

    .NewsSidebar-wys h2:not(:first-child),.NewsSidebar-wys h3:not(:first-child),.NewsSidebar-wys h4:not(:first-child),.NewsSidebar-wys h5:not(:first-child) {
        margin-top: 2.5em
    }

    .NewsSidebar-wys p {
        font-size: 1rem;
        font-weight: 100;
        letter-spacing: -.00625em;
        line-height: 1.8;
        margin-bottom: 1.5em
    }

    @media(min-width: 577px) {
        .NewsSidebar-wys ol,.NewsSidebar-wys ul {
            margin:6em auto
        }
    }

    @media(max-width: 576px) {
        .NewsSidebar-wys ol,.NewsSidebar-wys ul {
            margin:4em auto
        }
    }

    .NewsSidebar-wys ul li {
        grid-gap: 20px;
        display: grid;
        gap: 20px;
        grid-auto-flow: column;
        grid-template-columns: max-content auto
    }

    .NewsSidebar-wys ul li:before {
        background: #1efd8d;
        content: "";
        height: 24px;
        width: 2px
    }

    .NewsSidebar-wys li {
        font-size: 1.125rem;
        letter-spacing: -.0055555556em
    }

    .NewsSidebar-wys li+li {
        margin-top: .8em
    }

    .NewsSidebar-wys li p {
        margin-bottom: 0
    }

    @media(min-width: 1441px) {
        .NewsSidebar-wys--first p:first-of-type {
            font-size:1.625rem;
            letter-spacing: -.0230769231em
        }
    }

    @media(max-width: 1440px) {
        .NewsSidebar-wys--first p:first-of-type {
            font-size:1.25rem;
            letter-spacing: -.005em
        }
    }

    .NewsSidebar-blockquote {
        background-color: #262626;
        box-sizing: content-box;
        color: #fff;
        margin: 10% auto;
        padding: 10% 8.6vw
    }

    @media(max-width: 576px) {
        .NewsSidebar-blockquote {
            margin-bottom:30%;
            margin-top: 30%;
            padding-bottom: 30%;
            padding-top: 30%
        }
    }

    .NewsSidebar-blockquoteInner {
        margin: auto;
        max-width: 750px
    }

    .NewsSidebar-blockquoteContent {
        font-weight: 100
    }

    .NewsSidebar-blockquoteAuthor {
        grid-column-gap: 15px;
        align-items: center;
        -moz-column-gap: 15px;
        column-gap: 15px;
        display: grid;
        font-size: .9375rem;
        font-weight: 300;
        grid-auto-rows: max-content;
        grid-template-columns: max-content 1fr;
        padding-top: 50px
    }

    @media(max-width: 576px) {
        .NewsSidebar-blockquoteAuthor {
            padding-top:30px
        }
    }

    .NewsSidebar-blockquoteAuthorAvatar {
        border-radius: 100%;
        grid-row: span 2;
        height: 50px;
        overflow: hidden;
        position: relative;
        width: 50px;
        z-index: 1
    }

    .NewsSidebar-blockquoteAuthorName {
        color: #1efd8d;
        font-weight: 500;
        letter-spacing: -.0066666667em;
        padding-top: 4px
    }

    .NewsSidebar-blockquoteAuthorJobTitle {
        letter-spacing: -.0066666667em;
        opacity: .8;
        padding-bottom: 4px
    }

    .NewsSidebar-link,.NewsSidebar-share {
        align-items: center;
        cursor: pointer;
        display: flex;
        font-weight: 100;
        justify-content: space-between;
        padding-left: 60px;
        padding-right: 60px
    }

    @media(max-width: 576px) {
        .NewsSidebar-link,.NewsSidebar-share {
            font-size:1rem;
            padding-left: 8.6vw;
            padding-right: 8.6vw
        }
    }

    .NewsSidebar-link {
        background-color: #111;
        color: #fff;
        height: 12.5vw;
        margin-top: 10%;
        max-height: 200px
    }

    @media(max-width: 576px) {
        .NewsSidebar-link {
            height:24vw
        }

        .NewsSidebar-linkIcon {
            width: 18px
        }
    }

    .NewsSidebar-gridGallery {
        grid-gap: 10px;
        display: grid;
        gap: 10px;
        margin: 0 auto;
        max-width: 1010px
    }

    @media(min-width: 993px) {
        .NewsSidebar-gridGallery {
            grid-template-columns:repeat(2,1fr);
            padding: 0 60px
        }
    }

    .NewsSidebar-share {
        color: #111;
        height: 8.75vw;
        max-height: 140px
    }

    @media(max-width: 576px) {
        .NewsSidebar-share {
            height:20vw
        }

        .NewsSidebar-shareIcon {
            width: 18px
        }
    }

    .NewsSidebar-clipboard {
        grid-gap: 12px;
        align-items: center;
        box-sizing: content-box;
        cursor: pointer;
        display: grid;
        font-size: 1rem;
        gap: 12px;
        grid-template-columns: max-content auto;
        letter-spacing: -.00625em;
        margin: -8% auto 0;
        max-width: 750px;
        padding: 0 8.6vw
    }

    .NewsSidebar-clipboardConfirmation {
        grid-gap: 5px;
        align-items: center;
        background-color: #111;
        border-radius: 3px;
        bottom: 100px;
        color: #fff;
        display: grid;
        grid-auto-flow: column;
        left: 62.5%;
        padding: 5px 10px;
        pointer-events: none;
        position: fixed;
        transform: translateX(-50%)
    }

    .NewsSidebar-clipboardConfirmation.v-enter-active,.NewsSidebar-clipboardConfirmation.v-leave-active {
        transition: opacity .5s linear
    }

    .NewsSidebar-clipboardConfirmation.v-enter,.NewsSidebar-clipboardConfirmation.v-leave-to {
        opacity: 1;
    }

    .NewsSidebar-contentLink {
        align-items: flex-end;
        display: grid;
        grid-template-columns: 1fr max-content
    }

    @media(min-width: 577px) {
        .NewsSidebar-contentLink {
            margin-bottom:12%;
            margin-top: 12%;
            padding-left: 60px;
            padding-right: 60px
        }
    }

    @media(max-width: 576px) {
        .NewsSidebar-contentLink {
            margin-bottom:30%;
            margin-top: 30%;
            padding-left: 8.6vw;
            padding-right: 8.6vw
        }
    }

    .NewsSidebar-contentLinkLabel {
        font-size: 5rem;
        font-weight: 100;
        letter-spacing: -.01875em;
        line-height: 1
    }

    @media(max-width: 992px) {
        .NewsSidebar-contentLinkLabel {
            font-size:4.375rem
        }
    }

    @media(max-width: 767px) {
        .NewsSidebar-contentLinkLabel {
            font-size:3.125rem
        }
    }

    @media(max-width: 576px) {
        .NewsSidebar-contentLinkLabel {
            font-size:2.25rem
        }
    }

    .NewsSidebar-contentLinkIcon {
        margin-bottom: 15px
    }

    @media(max-width: 576px) {
        .NewsSidebar-contentLinkIcon {
            margin-bottom:-4px;
            width: 19px
        }
    }

    .NewsSidebar-nextArticle {
        grid-gap: 20px;
        align-content: flex-start;
        color: hsla(0,0%,7%,.5);
        cursor: pointer;
        display: grid;
        font-size: .875rem;
        gap: 20px;
        height: 23vw;
        justify-items: center;
        margin-top: 10%;
        overflow: hidden;
        text-align: center;
        text-transform: uppercase
    }

    @media(max-width: 992px) {
        .NewsSidebar-nextArticle {
            height:30vw
        }
    }

    @media(max-width: 576px) {
        .NewsSidebar-nextArticle {
            height:calc(var(--hero-height)/ 2 + 70px);
            margin-top: 30%
        }
    }

    .NewsSidebar-nextArticleImg {
        background-color: #fff;
        height: 100vh;
        transition: transform 1.2s cubic-bezier(.86,0,.07,1),padding 1.2s cubic-bezier(.86,0,.07,1);
        width: 100%
    }

    @media(min-width: 577px) {
        .NewsSidebar-nextArticleImg {
            padding:0 60px
        }
    }

    @media(max-width: 576px) {
        .NewsSidebar-nextArticleImg {
            padding:0 8.6vw
        }
    }

    .NewsSidebar-nextArticleImg--cloned {
        position: absolute
    }

    .NewsSidebar-backButton {
        color: #111;
        cursor: pointer;
        left: 8.6vw;
        position: fixed;
        top: 8.6vw;
        transform: scaleX(-1);
        z-index: 99999
    }

    @media screen and (min-width: 993px) {
        .NewsSidebar-backButton {
            display:none
        }
    }

    .NewsSidebar.v-enter-active .NewsSidebar-backButton,.NewsSidebar.v-leave-active .NewsSidebar-backButton {
        transition: opacity .2s linear
    }

    .NewsSidebar.v-enter-active .NewsSidebar-backButton {
        transition-duration: 1s
    }

    .NewsSidebar.v-enter .NewsSidebar-backButton,.NewsSidebar.v-leave-to .NewsSidebar-backButton {
        opacity: 0
    }

    .NewsTimeline {
        font-size: .875rem;
        line-height: 1.2;
        position: fixed;
        z-index: 2
    }

    .NewsTimeline,.NewsTimeline.is-disabled .NewsTimeline-month.is-active {
        color: hsla(0,0%,100%,.3)
    }

    .NewsTimeline.is-disabled .NewsTimeline-month.is-active span {
        transform: none
    }

    .NewsTimeline.is-disabled .NewsTimeline-month.is-active:before {
        background-color: hsla(0,0%,100%,.3);
        width: 40px!important
    }

    @media(min-width: 993px) {
        .NewsTimeline {
            top:50%
        }
    }

    @media(max-width: 992px) {
        .NewsTimeline {
            background-color:#111;
            overflow: auto;
            padding-bottom: 15px;
            padding-top: 104px;
            top: 0;
            width: 100vw
        }
    }

    @media(max-width: 576px) {
        .NewsTimeline {
            padding-top:80px;
            transition: padding-top 1s cubic-bezier(.165,.84,.44,1)
        }

        .is-down .NewsTimeline {
            padding-top: 20px
        }
    }

    .NewsTimeline-inner,.NewsTimeline-monthsList,.NewsTimeline-year {
        grid-gap: 25px;
        display: grid;
        gap: 25px
    }

    @media(max-width: 992px) {
        .NewsTimeline-inner,.NewsTimeline-monthsList,.NewsTimeline-year {
            grid-auto-flow:column
        }

        .NewsTimeline-inner {
            font-size: .75rem;
            padding-left: 8.6vw;
            padding-right: 8.6vw;
            width: -moz-fit-content;
            width: fit-content
        }
    }

    .NewsTimeline-month,.NewsTimeline-yearLabel {
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1),opacity .8s cubic-bezier(.77,0,.175,1)
    }

    .NewsTimeline-month[data-hidden],.NewsTimeline-yearLabel[data-hidden] {
        opacity: 1;
        transform: translateX(-100%)
    }

    @media(max-width: 767px) {
        .NewsTimeline-month[data-hidden],.NewsTimeline-yearLabel[data-hidden] {
            transform:translateX(100%)
        }
    }

    @media(min-width: 993px) {
        .NewsTimeline-yearLabel {
            padding-left:60px
        }
    }

    .NewsTimeline-month {
        align-items: center;
        cursor: pointer;
        display: flex;
        gap: 20px;
        position: relative
    }

    .NewsTimeline-month span {
        pointer-events: none;
        transform-origin: center;
        transition: transform .6s cubic-bezier(.77,0,.175,1),color .6s cubic-bezier(.77,0,.175,1)
    }

    @media(min-width: 993px) {
        .NewsTimeline-month span {
            transform-origin:left
        }
    }

    .NewsTimeline-month.is-active {
        color: #1efd8d
    }

    @media(min-width: 993px) {
        .NewsTimeline-month.is-active span {
            transform:scale(1.3)
        }
    }

    .NewsTimeline-month.is-active:before {
        background-color: #1efd8d;
        width: 100px
    }

    @media(min-width: 993px) {
        .NewsTimeline-month:before {
            background-color:hsla(0,0%,100%,.3);
            content: "";
            height: 1px;
            transition: width .6s cubic-bezier(.77,0,.175,1),background-color .6s cubic-bezier(.77,0,.175,1);
            width: 40px
        }
    }

    .NewsCardsList {
        grid-gap: 5px;
        display: grid;
        grid-auto-columns: 1fr;
        justify-content: flex-end
    }

    @media(min-width: 993px) {
        .NewsCardsList {
            margin-left:25vw;
            padding-top: 104px
        }
    }

    @media(max-width: 992px) {
        .NewsCardsList {
            padding-top:134px
        }
    }

    @media(max-width: 576px) {
        .NewsCardsList {
            padding-top:110px;
            transition: padding-top 1s cubic-bezier(.165,.84,.44,1)
        }

        .is-down .NewsCardsList {
            padding-top: 30px
        }
    }

    .NewsCardsList-item {
        opacity: 1;
        transform: translateY(100px);
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1),opacity .5s cubic-bezier(.77,0,.175,1)
    }

    @media(max-width: 576px) {
        .NewsCardsList-item {
            transform:translateY(200px)
        }
    }

    .is-loaded .NewsCardsList-item {
        opacity: 1;
        transform: none
    }

    .NewsCardsList-item:first-child {
        transition-delay: 0s
    }

    .NewsCardsList-item:nth-child(2) {
        transition-delay: .12s
    }

    .NewsCardsList-item:nth-child(3) {
        transition-delay: .24s
    }

    .NewsCardsList-item:nth-child(4) {
        transition-delay: .36s
    }

    .NewsCardsList-item:nth-child(5) {
        transition-delay: .48s
    }

    .NewsCardsList-item:nth-child(6) {
        transition-delay: .6s
    }

    .NewsCardsList-item:nth-child(7) {
        transition-delay: .72s
    }

    .NewsCardsList-item:nth-child(8) {
        transition-delay: .84s
    }

    .NewsCardsList-item:nth-child(9) {
        transition-delay: .96s
    }

    .NewsCardsList-item:nth-child(10) {
        transition-delay: 1.08s
    }

    .NewsCardsList-item:nth-child(11) {
        transition-delay: 1.2s
    }

    .NewsCardsList-item:nth-child(12) {
        transition-delay: 1.32s
    }

    .NewsCardsList-item:nth-child(13) {
        transition-delay: 1.44s
    }

    .NewsCardsList-item:nth-child(14) {
        transition-delay: 1.56s
    }

    .NewsCardsList-item:nth-child(15) {
        transition-delay: 1.68s
    }

    .NewsCardsList-item:nth-child(16) {
        transition-delay: 1.8s
    }

    .NewsCardsList-item:nth-child(17) {
        transition-delay: 1.92s
    }

    .NewsCardsList-item:nth-child(18) {
        transition-delay: 2.04s
    }

    .NewsCardsList-item:nth-child(19) {
        transition-delay: 2.16s
    }

    .NewsCardsList-item:nth-child(20) {
        transition-delay: 2.28s
    }

    .About .fp-tableCell {
        align-items: center;
        height: 100vh
    }

    @media(max-width: 1440px) {
        .About .fp-tableCell {
            flex-direction:row
        }
    }

    .About-image,.About-text {
        overflow: hidden
    }

    .About-image {
        height: 100%
    }

    .About-text {
        margin: 0 auto
    }

    @media(min-width: 993px) {
        .About-text {
            max-width:40vw
        }
    }

    .About-paragraph {
        color: rgba(0,0,0,.5)
    }

    @media(min-width: 769px)and (max-width:992px) {
        .About-paragraph {
            font-size:1rem
        }
    }

    @media(min-width: 577px)and (max-width:768px) {
        .About-paragraph {
            font-size:.9375rem
        }
    }

    @media(min-width: 993px) {
        .About-paragraph {
            font-size:1.25rem;
            line-height: 1.5
        }
    }

    .About-partners {
        margin-top: 1.875rem
    }

    .About-partnersList {
        display: flex;
        flex-wrap: wrap;
        gap: 5px
    }

    @media(max-width: 1440px) {
        .About-partnersList img {
            zoom:.8
        }
    }

    @media(max-width: 576px) {
        .About-partnersList img {
            zoom:.72
        }
    }

    .About-partnersListItemImg {
        transition: filter .5s linear
    }

    .About-partnersListItemImg:hover {
        filter: brightness(90%);
        transition-duration: .05s
    }

    .About-partnersLabel {
        color: rgba(0,0,0,.5);
        display: inline-block;
        font-size: .875rem;
        margin-bottom: 15px
    }

    @media(min-width: 1441px) {
        .Founder-text {
            display:flex!important;
            flex-direction: column;
            justify-content: center;
            padding-bottom: 3vh!important;
            padding-top: 3vh!important
        }
    }

    .Hiring-content {
        align-items: center;
        padding: 0!important
    }

    @media(max-width: 992px) {
        .Hiring-content {
            grid-row-gap:0!important;
            grid-auto-flow: dense!important
        }
    }

    .Hiring-title {
        padding: 6vh 0 6vh 9vw
    }

    @media(min-width: 769px) {
        .Hiring-title {
            width:50vw
        }
    }

    @media(min-width: 993px) {
        .Hiring-title {
            max-width:none!important
        }
    }

    @media(max-width: 992px) {
        .Hiring-title {
            margin-top:0!important
        }
    }

    .Hiring .JobCTA {
        font-size: 2.5rem;
        position: static;
        transform: none
    }

    @media(max-width: 1920px) {
        .Hiring .JobCTA {
            font-size:2rem
        }
    }

    @media(min-width: 993px) {
        .Hiring .JobCTA {
            padding:0 6vw
        }
    }

    @media(max-width: 992px)and (min-width:577px) {
        .Hiring .JobCTA {
            padding:calc(1vw + 50px) 9vw
        }
    }

    @media(max-width: 576px) {
        .Hiring .JobCTA {
            font-size:1.125rem
        }
    }

    .Hiring .JobCTA-icon {
        transform: rotate(90deg)
    }

    .Hiring-paragraphs {
        margin-left: 0!important;
        margin-right: 0!important;
        margin-top: 0!important;
        max-width: none!important;
        position: relative
    }

    @media(min-width: 993px) {
        .Hiring-paragraphs {
            height:33.3333333333vh
        }
    }

    .People {
        background: #111;
        cursor: none;
        z-index: 2
    }

    .People .fp-tableCell {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 10vh 0
    }

    .People .swiper-container {
        overflow: visible;
        overflow: initial
    }

    .People-header {
        color: #fff;
        margin-bottom: 2.5em
    }

    .People-header * {
        letter-spacing: 0
    }

    @media(min-width: 1441px) {
        .People-header {
            display:none
        }
    }

    @media(max-width: 1440px) {
        .People-header br {
            content:""
        }

        .People-header br:after {
            content: " "
        }
    }

    .People-subhead {
        color: hsla(0,0%,100%,.5)
    }

    .People-list {
        color: #fff
    }

    .People-listTitle {
        font-size: 5.625rem;
        letter-spacing: -.8px;
        line-height: .95;
        margin-bottom: .2em
    }

    .People-listSubhead {
        color: hsla(0,0%,100%,.5);
        display: grid;
        line-height: 1.125
    }

    .People-listHeader {
        margin-left: 120px!important;
        margin-right: 80px
    }

    @media(min-width: 577px) {
        .People-listHeader {
            width:380px!important
        }
    }

    @media(min-width: 1921px) {
        .People-listItem {
            margin-left:20px;
            width: 380px
        }
    }

    @media(max-width: 1920px) {
        .People-listItem {
            margin-left:16px;
            width: 300px
        }
    }

    @media(max-width: 992px) {
        .People-listItem {
            width:280px
        }
    }

    @media(max-width: 576px) {
        .People-listItem {
            margin-left:10px;
            width: 230px
        }
    }

    .People-listItem:not(.swiper-slide-duplicate) {
        opacity: 1;
        transform: translateX(140px);
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1),opacity .3s ease-in
    }

    .People-listItem:nth-child(3) {
        transform: none
    }

    @media(min-width: 460px) {
        .People-listItem:nth-child(4) {
            transform:none
        }
    }

    @media(min-width: 1110px) {
        .People-listItem:nth-child(5) {
            transform:none
        }
    }

    .active .People-listItem[data-swiper-slide-index="0"] {
        transition-delay: 1s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="0"] {
        transition-delay: 0s
    }

    .active .People-listItem[data-swiper-slide-index="1"] {
        transition-delay: 1.12s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="1"] {
        transition-delay: .12s
    }

    .active .People-listItem[data-swiper-slide-index="2"] {
        transition-delay: 1.24s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="2"] {
        transition-delay: .24s
    }

    .active .People-listItem[data-swiper-slide-index="3"] {
        transition-delay: 1.36s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="3"] {
        transition-delay: .36s
    }

    .active .People-listItem[data-swiper-slide-index="4"] {
        transition-delay: 1.48s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="4"] {
        transition-delay: .48s
    }

    .active .People-listItem[data-swiper-slide-index="5"] {
        transition-delay: 1.6s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="5"] {
        transition-delay: .6s
    }

    .active .People-listItem[data-swiper-slide-index="6"] {
        transition-delay: 1.72s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="6"] {
        transition-delay: .72s
    }

    .active .People-listItem[data-swiper-slide-index="7"] {
        transition-delay: 1.84s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="7"] {
        transition-delay: .84s
    }

    .active .People-listItem[data-swiper-slide-index="8"] {
        transition-delay: 1.96s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="8"] {
        transition-delay: .96s
    }

    .active .People-listItem[data-swiper-slide-index="9"] {
        transition-delay: 2.08s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="9"] {
        transition-delay: 1.08s
    }

    .active .People-listItem[data-swiper-slide-index="10"] {
        transition-delay: 2.2s
    }

    .is-safari .active .People-listItem[data-swiper-slide-index="10"] {
        transition-delay: 1.2s
    }

    .active .People-listItem,.complete .People-listItem {
        opacity: 1;
        transform: none
    }

    .People-member {
        perspective: 4000px
    }

    @media(min-width: 768px) {
        .People-member.is-flipped .People-memberInner {
            transform:rotateY(180deg)
        }
    }

    .People-memberInner {
        position: relative;
        transform-style: preserve-3d;
        transition: transform 1s cubic-bezier(.165,.84,.44,1);
        width: 100%
    }

    @media(min-width: 1921px) {
        .People-memberInner {
            height:660px
        }
    }

    @media(max-width: 1920px) {
        .People-memberInner {
            height:530px
        }
    }

    @media(max-width: 576px) {
        .People-memberInner {
            height:340px
        }
    }

    .People-memberInner.is-disabled {
        pointer-events: none
    }

    .People-memberSideA,.People-memberSideB {
        height: 100%;
        position: absolute;
        width: 100%
    }

    @media(min-width: 768px) {
        .People-memberSideA,.People-memberSideB {
            backface-visibility:hidden
        }
    }

    .People-memberSideA {
        display: grid;
        grid-template-rows: 1fr auto
    }

    .People-memberSideB {
        background-color: #fff;
        box-sizing: border-box;
        color: #111;
        transform: rotateY(180deg)
    }

    @media(min-width: 1441px) {
        .People-memberSideB {
            padding:50px 40px
        }
    }

    @media(max-width: 1440px) {
        .People-memberSideB {
            font-size:.875rem;
            padding: 40px 30px
        }
    }

    @media(max-width: 992px) {
        .People-memberSideB {
            font-size:.75rem
        }
    }

    @media(max-width: 767px) {
        .People-memberSideB {
            display:none
        }
    }

    .People-memberHeader {
        align-content: center;
        background-color: hsla(0,0%,85%,.05);
        color: #fff;
        display: grid;
        grid-auto-rows: max-content;
        padding-left: 30px;
        padding-right: 30px
    }

    @media(min-width: 1921px) {
        .People-memberHeader {
            height:150px
        }
    }

    @media(max-width: 1920px) {
        .People-memberHeader {
            height:115px
        }
    }

    @media(max-width: 576px) {
        .People-memberHeader {
            height:80px
        }
    }

    .People-memberName {
        margin-bottom: .2em
    }

    @media(min-width: 1921px) {
        .People-memberName {
            font-size:2rem
        }
    }

    @media(max-width: 1920px) {
        .People-memberName {
            font-size:1.625rem
        }
    }

    @media(max-width: 576px) {
        .People-memberName {
            font-size:1.125rem
        }
    }

    .People-memberJobTitle {
        color: hsla(0,0%,100%,.5)
    }

    @media(max-width: 576px) {
        .People-memberJobTitle {
            font-size:.875rem
        }
    }

    .People-memberMobileSidebar {
        -webkit-overflow-scrolling: touch;
        background-color: #fff;
        height: 100vh;
        left: 0;
        overflow: scroll;
        position: fixed;
        top: 0;
        width: 100vw;
        z-index: 100
    }

    .People-memberMobileSidebar.v-enter-active,.People-memberMobileSidebar.v-leave-active {
        transition: transform 1s cubic-bezier(.86,0,.07,1)
    }

    .People-memberMobileSidebar.v-enter,.People-memberMobileSidebar.v-leave-to {
        transform: translateX(100%)
    }

    .People-memberMobileSidebarInner {
        padding: 90px 30px 30px
    }

    .People-memberMobileSidebarBackBtn {
        color: #111;
        cursor: pointer;
        left: 30px;
        position: absolute;
        top: 30px;
        transform: scaleX(-1);
        z-index: 99999
    }

    .People-memberMobileSidebarContent {
        font-size: 1rem
    }

    .People-memberMobileSidebarContent.v-leave-to {
        visibility: hidden
    }

    .People-memberMobileSidebarContent.v-leave-active {
        transition: visibility 0s linear 1s
    }

    .People-memberInfos strong {
        color: #000;
        display: block;
        font-size: .625em;
        font-weight: 900;
        letter-spacing: .1em;
        margin-bottom: 3em;
        text-transform: uppercase
    }

    .People-memberInfos p {
        color: rgba(0,0,0,.6);
        font-size: 1em;
        line-height: 1.4;
        margin-bottom: 1em
    }

    @media(max-width: 1920px) {
        .People-memberInfos p {
            font-size:.8rem
        }
    }

    .BoardMembers {
        z-index: 2
    }

    @media(min-width: 993px) {
        .BoardMembers {
            background:linear-gradient(90deg,#f4f4f4 70%,#fff 0)
        }
    }

    .BoardMembers .swiper-container {
        height: 100%
    }

    @media(min-width: 1441px) {
        .BoardMembers .swiper-container {
            padding-left:33.3333333333vw
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .BoardMembers .swiper-container {
            padding-left:40vw
        }
    }

    .BoardMembers .swiper-wrapper {
        background-color: #fff
    }

    @media(max-width: 992px) {
        .BoardMembers-header {
            background-color:#f4f4f4
        }
    }

    @media(min-width: 993px) {
        .BoardMembers-header {
            align-content:center
        }
    }

    @media(min-width: 1441px) {
        .BoardMembers-title {
            font-size:1.75rem
        }
    }

    @media(max-width: 1440px) {
        .BoardMembers-title {
            font-size:1.5rem
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-title {
            font-size:.9375rem
        }
    }

    .BoardMembers-body {
        cursor: none;
        position: static!important;
        width: 100vw
    }

    @media(max-width: 992px) {
        .BoardMembers-body {
            height:768px
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-body {
            height:460px
        }
    }

    .BoardMembers-list {
        height: 100%;
        left: 0;
        position: absolute;
        width: 100vw
    }

    .BoardMembers-listItem {
        background-color: #fff;
        opacity: 1;
        transform: translateX(140px);
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1),opacity .3s ease-in
    }

    @media(min-width: 1441px) {
        .BoardMembers-listItem {
            width:350px
        }
    }

    @media(max-width: 1440px) {
        .BoardMembers-listItem {
            width:300px
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-listItem {
            width:160px
        }
    }

    .active .BoardMembers-listItem:first-child {
        transition-delay: 1s
    }

    .active .BoardMembers-listItem:nth-child(2) {
        transition-delay: 1.12s
    }

    .active .BoardMembers-listItem:nth-child(3) {
        transition-delay: 1.24s
    }

    .active .BoardMembers-listItem:nth-child(4) {
        transition-delay: 1.36s
    }

    .active .BoardMembers-listItem:nth-child(5) {
        transition-delay: 1.48s
    }

    .active .BoardMembers-listItem:nth-child(6) {
        transition-delay: 1.6s
    }

    .active .BoardMembers-listItem:nth-child(7) {
        transition-delay: 1.72s
    }

    .active .BoardMembers-listItem:nth-child(8) {
        transition-delay: 1.84s
    }

    .active .BoardMembers-listItem:nth-child(9) {
        transition-delay: 1.96s
    }

    .active .BoardMembers-listItem:nth-child(10) {
        transition-delay: 2.08s
    }

    .active .BoardMembers-listItem:nth-child(11) {
        transition-delay: 2.2s
    }

    .active .BoardMembers-listItem,.complete .BoardMembers-listItem {
        opacity: 1;
        transform: none
    }

    .BoardMembers-memberBody {
        color: #111;
        cursor: auto;
        display: flex;
        flex-direction: column;
        gap: 5px;
        justify-content: flex-start
    }

    @media(min-width: 1441px) {
        .BoardMembers-memberBody {
            padding:40px
        }
    }

    @media(max-width: 1440px) {
        .BoardMembers-memberBody {
            padding:35px
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-memberBody {
            padding:15px
        }
    }

    @media(min-width: 1441px) {
        .BoardMembers-memberPhoto {
            height:400px
        }
    }

    @media(max-width: 1440px) {
        .BoardMembers-memberPhoto {
            height:320px
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-memberPhoto {
            height:170px
        }
    }

    .BoardMembers-memberName {
        margin-bottom: .2em
    }

    @media(min-width: 1441px) {
        .BoardMembers-memberName {
            font-size:1.75rem
        }
    }

    @media(max-width: 1440px) {
        .BoardMembers-memberName {
            font-size:1.5rem
        }
    }

    @media(max-width: 576px) {
        .BoardMembers-memberName {
            font-size:.9375rem
        }
    }

    .BoardMembers-memberJobTitle {
        opacity: .5
    }

    .BoardMembers-memberLink:hover {
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .BoardMembers .DragCursor:after,.BoardMembers .DragCursor:before {
        background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg viewBox='0 0 7 12' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M6 1 1 6l5 5' stroke='%23111' stroke-width='1.5' fill='none' fill-rule='evenodd'/%3E%3C/svg%3E")
    }

    .Header {
        display: flex;
        justify-content: space-between;
        pointer-events: none;
        position: fixed;
        transition: transform 1s cubic-bezier(.77,0,.175,1),opacity 1s linear,-webkit-clip-path 1s cubic-bezier(.165,.84,.44,1);
        transition: transform 1s cubic-bezier(.77,0,.175,1),opacity 1s linear,clip-path 1s cubic-bezier(.165,.84,.44,1);
        transition: transform 1s cubic-bezier(.77,0,.175,1),opacity 1s linear,clip-path 1s cubic-bezier(.165,.84,.44,1),-webkit-clip-path 1s cubic-bezier(.165,.84,.44,1);
        width: 100%;
        z-index: 200
    }

    @media(min-width: 993px) {
        .Header {
            padding:0;
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Header {
            padding:40;
        }
    }

    @media(max-width: 576px) {
        .Header {
            padding:30px 0 0 0;
        }
    }

    .Header.is-sticky {
        background-color: hsla(0,0%,7%,.5);
        position: fixed
    }

    @media(min-width: 993px) {
        .Header.is-sticky {
            padding-bottom:20px
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .Header.is-sticky {
            padding-bottom:20px
        }
    }

    .is-down .Header.is-sticky {
        transform: translateY(-100%)
    }

    @media(max-width: 576px) {
        [class*=page-news] .Header,[class*=page-projects] .Header {
            -webkit-clip-path:inset(0 0 30px 0);
            clip-path: inset(0 0 30px 0)
        }

        [class*=page-news].is-down .Header,[class*=page-projects].is-down .Header {
            -webkit-clip-path: inset(0 0 100px 0);
            clip-path: inset(0 0 100px 0)
        }
    }

    .sidebar-open .Header {
        opacity: 1;
    }

    @media(max-width: 992px) {
        .has-banner .Header {
            transform:translateY(32px)
        }
    }

    @media(min-width: 993px) {
        .has-banner .Header {
            transform:translateY(36px)
        }
    }

    .Header-title {
        font-size: 0
    }

    .Footer {
        background: #111;
        color: #fff;
        padding: 6vh 8.6vw;
        position: relative
    }

    .Footer,.Footer .fp-tableCell {
        display: grid;
        width: 100%
    }

    @media(min-width: 993px) {
        .Footer,.Footer .fp-tableCell {
            grid-template-columns:1fr auto auto;
            grid-template-rows: repeat(3,max-content)
        }
    }

    @media(max-width: 992px) {
        .Footer,.Footer .fp-tableCell {
            grid-row-gap:60px;
            grid-template-columns: max-content 1fr
        }
    }

    @media(min-width: 993px) {
        .Footer-informations {
            grid-row:span 2;
            max-width: 420px;
            padding-right: 80px
        }
    }

    @media(max-width: 992px) {
        .Footer-informations {
            grid-column:span 2;
            max-width: 280px
        }
    }

    .Footer-langSwitcher {
        font-size: 12px;
        margin-top: 30px
    }

    @media(max-width: 767px) {
        .Footer-langSwitcher {
            margin-top:50px
        }
    }

    .Footer-link {
        color: #fff
    }

    .Footer-link.nuxt-link-exact-active {
        position: relative
    }

    .Footer-link.nuxt-link-exact-active:before {
        background: #1efd8d;
        border-radius: 100%;
        content: "";
        height: 4px;
        left: -12px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 4px
    }

    .Footer-legalLink {
        color: #fff;
        display: inline-block;
        font-size: 10px
    }

    @media(max-width: 992px) {
        .Footer-form {
            display:grid;
            grid-column: span 2;
            justify-content: flex-start
        }
    }

    @media(min-width: 1441px) {
        .Footer-nav {
            padding-right:10vw
        }
    }

    @media(max-width: 1440px) {
        .Footer-nav {
            padding-right:60px
        }
    }

    @media(min-width: 993px) {
        .Footer-nav {
            grid-row:span 2;
            padding-top: 30px
        }
    }

    @media(max-width: 992px) {
        .Footer-nav {
            padding-right:90px
        }
    }

    .Footer-links {
        grid-gap: 12px;
        display: grid
    }

    .Footer-social {
        grid-gap: 12px 30px;
        display: grid;
        grid-template: max-content/max-content
    }

    @media(min-width: 993px) {
        .Footer-social {
            grid-auto-flow:column;
            justify-content: flex-start;
            padding-bottom: 60px;
            padding-top: 30px
        }
    }

    @media(max-width: 992px) {
        .Footer-social {
            align-content:flex-start
        }
    }

    .Footer-social .Footer-link {
        opacity: .5
    }

    .Footer-social .Footer-link:hover {
        opacity: 1
    }

    .Footer-bottom {
        align-items: flex-end;
        display: flex;
        justify-content: space-between;
        padding-top: 35px;
        width: 100%
    }

    @media(min-width: 993px) {
        .Footer-bottom {
            grid-column:span 3
        }
    }

    @media(max-width: 992px) {
        .Footer-bottom {
            grid-column:span 2
        }
    }

    .Footer-bottomLegal {
        display: flex;
        gap: 10px
    }

    @media(max-width: 767px) {
        .Footer-bottomLegal {
            flex-direction:column
        }
    }

    .Footer-copyright {
        display: inline-block;
        font-size: 10px;
        opacity: .5;
        text-transform: uppercase
    }

    .Footer-backToTop {
        align-items: flex-start;
        color: #fff;
        cursor: pointer;
        display: flex;
        font-size: 11px;
        opacity: .5;
        text-transform: uppercase
    }

    @media(max-width: 992px)and (min-width:577px) {
        .Footer-backToTop {
            position:absolute;
            right: 8.6vw;
            top: 100px
        }
    }

    .Footer-backToTop:hover {
        opacity: 1
    }

    .Footer-backToTop:hover .Footer-backToTopIcon {
        transform: translateY(-30%)
    }

    .Footer-backToTopIcon {
        margin-left: 10px;
        transition: transform .3s cubic-bezier(.23,1,.32,1);
        will-change: transform
    }

    .LayoutTwo-dark {
        background-color: #111;
        color: #fff
    }

    .LayoutTwo-media {
        overflow: hidden;
        position: relative;
        z-index: 1
    }

    .LayoutTwo-text {
        grid-row-gap: 1.875rem;
        display: grid;
        grid-auto-rows: max-content
    }

    @media(max-width: 992px) {
        .LayoutTwo-text {
            padding:50px 8.6vw
        }
    }

    .LayoutTwo-paragraphs {
        grid-gap: 1.25rem 2vw;
        display: grid
    }

    .LayoutTwo-paragraphs ol,.LayoutTwo-paragraphs ul {
        grid-gap: .5rem;
        display: grid
    }

    .LayoutTwo-paragraphs a {
        color: currentColor;
        font-weight: 500;
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .LayoutTwo-paragraphs li {
        grid-gap: 10px;
        display: grid;
        grid-template-columns: max-content 1fr
    }

    .LayoutTwo-paragraphs li:before {
        background-color: hsla(0,0%,7%,.25);
        content: "";
        height: 12px;
        position: relative;
        top: 4px;
        width: 1.4px
    }

    @media(max-width: 992px)and (min-width:577px) {
        .LayoutTwo-split {
            grid-gap:2vw;
            display: grid;
            grid-auto-columns: 1fr;
            grid-auto-flow: column
        }
    }

    @media(min-width: 577px)and (max-width:992px) {
        .LayoutTwo-split header {
            margin-top:-.5rem
        }
    }

    @media(min-width: 993px) {
        .LayoutTwo-horizontal .LayoutTwo-size30 {
            height:33.3333333333vh
        }

        .LayoutTwo-horizontal .LayoutTwo-size70 {
            height: 66.6666666667vh
        }
    }

    @media(min-width: 577px) {
        .LayoutTwo-horizontal .LayoutTwo-size50 {
            height:50%
        }
    }

    .LayoutTwo-horizontal .LayoutTwo-text {
        display: grid
    }

    @media(min-width: 993px) {
        .LayoutTwo-horizontal .LayoutTwo-text {
            grid-column-gap:4vw;
            grid-template-columns: fit-content(50%) auto;
            height: 33.3333333333vh;
            padding: 6vh 9vw
        }
    }

    @media(max-width: 992px) {
        .LayoutTwo-horizontal .LayoutTwo-text {
            grid-column-gap:2vw
        }
    }

    @media(min-width: 577px) {
        .LayoutTwo-horizontal .LayoutTwo-text {
            grid-auto-columns:1fr;
            grid-auto-flow: column
        }
    }

    @media(min-width: 993px) {
        .LayoutTwo-horizontal .LayoutTwo-paragraphs {
            grid-auto-flow:column;
            margin: auto;
            max-width: 48vw
        }
    }

    .LayoutTwo-horizontal .LayoutTwo-paragraphs li,.LayoutTwo-horizontal .LayoutTwo-paragraphs p,.LayoutTwo-horizontal .Paragraph,.LayoutTwo-horizontal header,.LayoutTwo-paragraphs .LayoutTwo-horizontal li,.LayoutTwo-paragraphs .LayoutTwo-horizontal p {
        max-width: 480px
    }

    @media(min-width: 577px) {
        .LayoutTwo-horizontal header {
            margin-top:-.5rem
        }
    }

    .LayoutTwo-vertical>* {
        display: flex
    }

    @media(max-width: 992px) {
        .LayoutTwo-vertical>* {
            flex-direction:column;
            flex-wrap: wrap
        }
    }

    @media(min-width: 1441px) {
        .LayoutTwo-vertical .LayoutTwo-size30 {
            width:33.3333333333%
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .LayoutTwo-vertical .LayoutTwo-size30 {
            width:40%
        }
    }

    @media(min-width: 1441px) {
        .LayoutTwo-vertical .LayoutTwo-size70 {
            width:66.6666666667%
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .LayoutTwo-vertical .LayoutTwo-size70 {
            width:60%
        }
    }

    @media(min-width: 993px) {
        .LayoutTwo-vertical .LayoutTwo-size50 {
            width:50%
        }
    }

    @media(max-width: 992px) {
        .LayoutTwo-vertical .LayoutTwo-size50 {
            width:100%
        }
    }

    .LayoutTwo-vertical .LayoutTwo-size100 {
        width: 100%
    }

    @media(min-width: 1441px) {
        .LayoutTwo-vertical .LayoutTwo-text {
            padding:20vh 4.8vw
        }
    }

    @media(min-width: 993px)and (max-width:1440px) {
        .LayoutTwo-vertical .LayoutTwo-text {
            padding:16vh 3.4vw
        }
    }

    @media(max-width: 992px) {
        .LayoutTwo-mobileMask {
            position:relative
        }

        .LayoutTwo-mobileMask:before {
            background: #fff;
            content: "";
            display: block;
            height: 100%;
            position: absolute;
            transform: scaleX(1);
            transform-origin: right;
            transition: transform 1.2s cubic-bezier(.77,0,.175,1);
            width: 100%;
            will-change: transform;
            z-index: 1
        }

        .LayoutTwo-dark .LayoutTwo-mobileMask:before {
            background: #111
        }

        .complete .LayoutTwo-mobileMask:before {
            transform: scaleX(0)
        }

        .LayoutTwo-mobileMask--fromLeft:not(.LayoutTwo-mobileMask--full) {
            margin-right: 8.6vw
        }

        .LayoutTwo-mobileMask--fromLeft:before {
            transform-origin: right
        }

        .LayoutTwo-mobileMask--fromRight:not(.LayoutTwo-mobileMask--full) {
            margin-left: 8.6vw
        }

        .LayoutTwo-mobileMask--fromRight:before {
            transform-origin: left
        }
    }

    .Menu {
        -webkit-overflow-scrolling: touch;
        bottom: 0;
        left: 0;
        overflow: auto;
        position: fixed;
        right: 0;
        top: 0;
        z-index: 100
    }

    @media(min-width: 993px) {
        @-moz-document url-prefix() {
            .Menu {
                scrollbar-width:none
            }
        }

        .Menu::-webkit-scrollbar {
            display: none;
            scrollbar-width: none
        }
    }

    .Menu-inner {
        align-items: flex-start;
        box-sizing: content-box;
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        max-width: 1000px;
        padding-bottom: 104px
    }

    @media(min-width: 993px) {
        .Menu-inner {
            padding-left:15vw;
            padding-right: 15vw;
            padding-top: 104px
        }
    }

    @media(max-width: 767px) {
        .Menu-inner {
            flex-direction:column;
            gap: 4em
        }
    }

    @media(max-width: 992px) {
        .Menu-inner {
            margin-top:104px;
            max-width: 640px;
            padding-left: 8.6vw;
            padding-right: 8.6vw
        }
    }

    @media(max-width: 576px) {
        .Menu-inner {
            margin-top:100px
        }
    }

    @media(max-width: 992px) {
        .has-banner .Menu-inner {
            margin-top:160px
        }
    }

    @media(max-width: 576px) {
        .has-banner .Menu-inner {
            margin-top:132px
        }
    }

    .Menu-backdrop {
        -webkit-backdrop-filter: blur(6px);
        backdrop-filter: blur(6px);
        background-color: hsla(0,0%,7%,.8);
        bottom: 0;
        display: block;
        left: 0;
        position: fixed;
        right: 0;
        top: 0;
        z-index: -1
    }

    .Menu.v-enter-active,.Menu.v-leave-active {
        transition: all 1s linear
    }

    .Menu.v-enter-active .Menu-aside,.Menu.v-enter-active .Menu-langSwitcher,.Menu.v-enter-active .Menu-nav,.Menu.v-leave-active .Menu-aside,.Menu.v-leave-active .Menu-langSwitcher,.Menu.v-leave-active .Menu-nav {
        transition: transform .8s cubic-bezier(.165,.84,.44,1),opacity .6s cubic-bezier(.77,0,.175,1)
    }

    .Menu.v-enter-active .Menu-backdrop,.Menu.v-leave-active .Menu-backdrop {
        transition: opacity .2s linear,-webkit-backdrop-filter .2s linear;
        transition: opacity .2s linear,backdrop-filter .2s linear;
        transition: opacity .2s linear,backdrop-filter .2s linear,-webkit-backdrop-filter .2s linear
    }

    .Menu.v-leave-active .Menu-aside,.Menu.v-leave-active .Menu-langSwitcher,.Menu.v-leave-active .Menu-nav {
        transition-duration: .8s,.4s;
        transition-timing-function: cubic-bezier(.77,0,.175,1)
    }

    .Menu.v-leave-active .Menu-backdrop {
        transition-delay: .3s
    }

    .Menu.v-enter .Menu-backdrop,.Menu.v-leave-to .Menu-backdrop {
        opacity: 0
    }

    .Menu.v-enter .Menu-aside,.Menu.v-enter .Menu-langSwitcher,.Menu.v-enter .Menu-nav,.Menu.v-leave-to .Menu-aside,.Menu.v-leave-to .Menu-langSwitcher,.Menu.v-leave-to .Menu-nav {
        opacity: 0;
        transform: scale(.88)
    }

    .Menu.v-enter .Menu-close,.Menu.v-leave-to .Menu-close {
        opacity: 0
    }

    .Menu-link {
        color: #fff;
        font-size: 3.75rem;
        height: 100%
    }

    @media(max-width: 1440px) {
        .Menu-link {
            font-size:3.125rem
        }
    }

    @media(max-width: 992px) {
        .Menu-link {
            font-size:2.25rem
        }
    }

    .Menu-links {
        display: grid;
        grid-auto-rows: max-content
    }

    @media(max-width: 767px) {
        .Menu-links {
            gap:.25em
        }
    }

    .Menu-links li {
        display: flex
    }

    .Menu-langSwitcher {
        font-size: 20px;
        padding-top: 130px
    }

    @media(max-width: 767px) {
        .Menu-langSwitcher {
            padding-top:50px
        }
    }

    .Menu-aside {
        max-width: 320px;
        width: 100%
    }

    .Menu-link {
        margin-left: -25px;
        padding-left: 25px
    }

    .Menu-link.is-inactive {
        color: hsla(0,0%,100%,.5)
    }

    .Menu-link:hover {
        color: #1efd8d!important
    }

    .Menu-link.nuxt-link-exact-active {
        pointer-events: none;
        position: relative
    }

    .Menu-link.nuxt-link-exact-active:before {
        background: #1efd8d;
        border-radius: 100%;
        content: "";
        left: 0;
        opacity: 1;
        position: absolute;
        top: 50%;
        transform: translateY(-50%)
    }

    @media(min-width: 577px) {
        .Menu-link.nuxt-link-exact-active:before {
            height:10px;
            width: 10px
        }
    }

    @media(max-width: 576px) {
        .Menu-link.nuxt-link-exact-active:before {
            height:5px;
            left: 10px;
            width: 5px
        }
    }

    .Menu-close {
        color: #fff;
        cursor: pointer;
        position: fixed;
        right: 40px;
        top: 40px;
        z-index: 20
    }

    @media(max-width: 767px) {
        .Menu-close {
            top:40px
        }
    }

    @media(max-width: 576px) {
        .Menu-close {
            top:30px
        }
    }

    .has-banner .Menu-close {
        top: 75px
    }

    @media(max-width: 767px) {
        .has-banner .Menu-close {
            top:60px
        }

        .Menu-closeIcon {
            height: 16px;
            width: 16px
        }
    }

    .Menu-nav {
        grid-gap: 20px;
        display: grid;
        gap: 20px
    }

    .Menu-newsList {
        grid-gap: 10px;
        display: grid;
        gap: 10px;
        padding-top: 1.5rem
    }

    .Menu-newsCard {
        background-color: #262626;
        border-radius: 5px;
        cursor: pointer;
        max-width: 320px;
        overflow: hidden;
        padding-bottom: 56.25%;
        position: relative;
        transition: background-color .3s linear;
        width: 100%
    }

    @media(min-width: 768px)and (max-width:992px) {
        .Menu-newsCard {
            max-width:260px
        }
    }

    .Menu-newsCard.is-loading {
        background-color: hsla(0,0%,100%,.1)
    }

    .Menu-newsCard:hover .Menu-newsCardFigure {
        transform: scale(1.05)
    }

    .Menu-newsCard>.v-enter,.Menu-newsCard>.v-leave-to {
        opacity: 1;
    }

    .Menu-newsCard>.v-enter-active,.Menu-newsCard>.v-leave-active {
        transition: opacity .3s linear
    }

    .Menu-newsCardFigure {
        height: 100%;
        position: absolute;
        transition: transform 1.2s cubic-bezier(.165,.84,.44,1)
    }

    .Menu-newsCardFigure:after {
        background-image: linear-gradient(180deg,hsla(0,0%,7%,0),#111);
        bottom: 0;
        content: "";
        left: 0;
        position: absolute;
        right: 0;
        top: 50%
    }

    .Menu-newsCardLink {
        bottom: 0;
        left: 0;
        position: absolute;
        right: 0;
        top: 0
    }

    .Menu-newsCardTitle {
        bottom: 0;
        color: #fff;
        font-size: .875rem;
        letter-spacing: -.0285714286em;
        padding: 12px;
        position: absolute
    }

    .Menu-newsMore {
        align-items: center;
        color: #fff;
        display: flex;
        font-size: 1.25rem;
        justify-content: space-between;
        max-width: 320px;
        padding-top: 20px;
        position: relative
    }

    .Menu-newsMore:hover {
        color: #1efd8d
    }

    .Menu-newsMore .Menu-link {
        font-size: inherit;
        width: 100%
    }

    @media(min-width: 768px)and (max-width:992px) {
        .Menu-newsMore {
            max-width:260px
        }
    }

    .Menu-newsMore:hover .Menu-newsMoreIcon {
        transform: rotate(90deg) translateY(-15px)
    }

    .Menu-newsMoreIcon {
        position: absolute;
        right: 0;
        transform: rotate(90deg);
        transition: transform .8s cubic-bezier(.23,1,.32,1)
    }

    .Menu .SubscribeForm {
        padding-top: 60px
    }

    .Menu .SubscribeForm-input {
        background-color: transparent;
        border-bottom: 1px solid hsla(0,0%,100%,.3);
        padding-left: 0;
        padding-right: 0
    }

    .Menu .SubscribeForm-input:not(:-moz-placeholder-shown):valid+.SubscribeForm-submit {
        color: #fff
    }

    .Menu .SubscribeForm-input:not(:placeholder-shown):valid+.SubscribeForm-submit {
        color: #fff
    }

    .Menu .SubscribeForm-input:not(:-moz-placeholder-shown):valid+.SubscribeForm-submit:hover {
        color: #1efd8d
    }

    .Menu .SubscribeForm-input:not(:placeholder-shown):valid+.SubscribeForm-submit:hover {
        color: #1efd8d
    }

    .Menu .SubscribeForm-label {
        color: #fff;
        font-size: 1rem;
        letter-spacing: 0;
        margin-bottom: .5em;
        white-space: nowrap
    }

    .Menu .SubscribeForm-submit {
        background-color: transparent;
        border-bottom: 1px solid hsla(0,0%,100%,.3);
        color: hsla(0,0%,100%,.5);
        padding-left: 10px;
        padding-right: 10px
    }

    .Menu .SubscribeForm-submit:before {
        bottom: -1px;
        height: 1px;
        top: auto
    }

    .u-color-offWhite {
        color: #f4f4f4
    }

    .u-color-pineGreen {
        color: #0b2819
    }

    .u-color-charcoal {
        color: #111
    }

    .u-color-lightGreenishBlue {
        color: #1efd8d
    }

    .u-inlineBlock {
        display: inline-block
    }

    .u-block {
        display: block
    }

    .u-hidden {
        display: none
    }

    @media(min-width: 1441px) {
        .u-hidden--lg-up {
            display:none
        }
    }

    @media(max-width: 1440px) {
        .u-hidden--lg {
            display:none
        }
    }

    @media(min-width: 993px) {
        .u-hidden--md-up {
            display:none
        }
    }

    @media(max-width: 992px) {
        .u-hidden--md {
            display:none
        }
    }

    @media(min-width: 769px) {
        .u-hidden--sm-up {
            display:none
        }
    }

    @media(max-width: 768px) {
        .u-hidden--sm {
            display:none
        }
    }

    @media(min-width: 577px) {
        .u-hidden--xs-up {
            display:none
        }
    }

    @media(max-width: 576px) {
        .u-hidden--xs {
            display:none
        }
    }

    .u-mx-auto {
        margin-left: auto
    }

    .u-mr-auto,.u-mx-auto {
        margin-right: auto
    }

    .u-ml-auto {
        margin-left: auto
    }

    .u-mb-0 {
        margin-bottom: 0!important
    }

    .u-mb-5 {
        margin-bottom: .3125rem!important
    }

    .u-mb-10 {
        margin-bottom: .625rem!important
    }

    .u-mb-15 {
        margin-bottom: .9375rem!important
    }

    .u-mb-20 {
        margin-bottom: 1.25rem!important
    }

    .u-mb-30 {
        margin-bottom: 1.875rem!important
    }

    .u-mb-50 {
        margin-bottom: 3.125rem!important
    }

    @media(min-width: 1441px) {
        .u-mb-0--lg-up {
            margin-bottom:0!important
        }

        .u-mb-5--lg-up {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--lg-up {
            margin-bottom: .625rem!important
        }

        .u-mb-15--lg-up {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--lg-up {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--lg-up {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--lg-up {
            margin-bottom: 3.125rem!important
        }
    }

    @media(max-width: 1440px) {
        .u-mb-0--lg {
            margin-bottom:0!important
        }

        .u-mb-5--lg {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--lg {
            margin-bottom: .625rem!important
        }

        .u-mb-15--lg {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--lg {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--lg {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--lg {
            margin-bottom: 3.125rem!important
        }
    }

    @media(min-width: 993px) {
        .u-mb-0--md-up {
            margin-bottom:0!important
        }

        .u-mb-5--md-up {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--md-up {
            margin-bottom: .625rem!important
        }

        .u-mb-15--md-up {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--md-up {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--md-up {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--md-up {
            margin-bottom: 3.125rem!important
        }
    }

    @media(max-width: 992px) {
        .u-mb-0--md {
            margin-bottom:0!important
        }

        .u-mb-5--md {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--md {
            margin-bottom: .625rem!important
        }

        .u-mb-15--md {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--md {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--md {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--md {
            margin-bottom: 3.125rem!important
        }
    }

    @media(min-width: 769px) {
        .u-mb-0--sm-up {
            margin-bottom:0!important
        }

        .u-mb-5--sm-up {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--sm-up {
            margin-bottom: .625rem!important
        }

        .u-mb-15--sm-up {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--sm-up {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--sm-up {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--sm-up {
            margin-bottom: 3.125rem!important
        }
    }

    @media(max-width: 768px) {
        .u-mb-0--sm {
            margin-bottom:0!important
        }

        .u-mb-5--sm {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--sm {
            margin-bottom: .625rem!important
        }

        .u-mb-15--sm {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--sm {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--sm {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--sm {
            margin-bottom: 3.125rem!important
        }
    }

    @media(min-width: 577px) {
        .u-mb-0--xs-up {
            margin-bottom:0!important
        }

        .u-mb-5--xs-up {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--xs-up {
            margin-bottom: .625rem!important
        }

        .u-mb-15--xs-up {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--xs-up {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--xs-up {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--xs-up {
            margin-bottom: 3.125rem!important
        }
    }

    @media(max-width: 576px) {
        .u-mb-0--xs {
            margin-bottom:0!important
        }

        .u-mb-5--xs {
            margin-bottom: .3125rem!important
        }

        .u-mb-10--xs {
            margin-bottom: .625rem!important
        }

        .u-mb-15--xs {
            margin-bottom: .9375rem!important
        }

        .u-mb-20--xs {
            margin-bottom: 1.25rem!important
        }

        .u-mb-30--xs {
            margin-bottom: 1.875rem!important
        }

        .u-mb-50--xs {
            margin-bottom: 3.125rem!important
        }
    }

    @media(min-width: 993px) {
        .u-mediaZoomAnimation img,.u-mediaZoomAnimation video {
            transform:scale(1.3);
            transition: transform 2.4s cubic-bezier(.165,.84,.44,1) .2s;
            will-change: transform
        }

        .u-mediaZoomAnimation img .is-safari,.u-mediaZoomAnimation video .is-safari {
            transition-delay: 0s
        }

        .active .u-mediaZoomAnimation img,.active .u-mediaZoomAnimation video,.complete .u-mediaZoomAnimation img,.complete .u-mediaZoomAnimation video {
            transform: scale(1)
        }
    }

    .u-mediaFullWidth {
        height: auto;
        width: 100%
    }

    .u-mediaFluid {
        height: auto;
        max-width: 100%
    }

    .u-mediaContain {
        height: 100%;
        -o-object-fit: contain;
        object-fit: contain;
        width: 100%
    }

    .u-mediaCover {
        height: 100%;
        -o-object-fit: cover;
        object-fit: cover;
        width: 100%
    }

    .u-mediaFullSize {
        display: block;
        position: absolute;
        z-index: -1
    }

    @media(max-width: 992px) {
        .u-mediaFullSize:not(.u-mediaFullSize--absolute) {
            position:static
        }
    }

    @supports not (-ms-ime-align:auto) {
        .u-mediaFullSize {
            height: 100%;
            left: 0;
            -o-object-fit: cover;
            object-fit: cover;
            top: 0;
            width: 100%
        }
    }

    @supports(-ms-ime-align:auto) {
        .u-mediaFullSize {
            height: auto;
            left: 50%;
            min-height: 100%;
            min-width: 100%;
            top: 50%;
            transform: translate(-50%,-50%);
            width: auto
        }
    }

    .u-relative {
        position: relative
    }

    .u-absolute {
        position: absolute
    }

    .u-textCenter {
        text-align: center
    }

    .u-textCapitalize:first-letter,.u-textUppercase {
        text-transform: uppercase
    }

    .u-textItalic {
        font-style: italic
    }

    .u-textCurrentColor {
        color: currentColor!important
    }

    .u-textUnderlined {
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .Contact {
        background: #111
    }

    @media(min-width: 993px) {
        .Contact {
            min-height:100vh
        }

        .Contact>* {
            height: 100vh
        }
    }

    @media(max-width: 992px) {
        .Contact-map {
            height:60vh
        }
    }

    @media(min-width: 993px) {
        .Contact-map {
            width:60%
        }
    }

    .Contact-map .vue-map-container {
        height: 100%
    }

    .Contact-map-text {
        color: #fff;
        left: 9vw;
        pointer-events: none;
        position: absolute;
        z-index: 20
    }

    @media(max-width: 993px) {
        .Contact-map-text {
            bottom:6vh
        }
    }

    @media(min-width: 993px) {
        .Contact-map-text {
            bottom:10vh
        }
    }

    @media(max-width: 576px) {
        .Contact-map-text {
            display:none
        }
    }

    .Contact-text {
        color: #f4f4f4
    }

    @media(min-width: 993px) {
        .Contact-text {
            width:40%
        }
    }

    .Contact-links {
        align-items: flex-start;
        display: flex;
        flex-direction: column
    }

    .Contact-links a {
        color: #1efd8d;
        position: relative;
        -webkit-text-decoration: none;
        text-decoration: none
    }

    .Contact-links a:hover:after {
        transform: scaleX(1);
        transform-origin: left;
        transition-timing-function: cubic-bezier(.165,.84,.44,1)
    }

    .Contact-links a:after {
        background: currentColor;
        content: "";
        height: 1px;
        left: 0;
        position: absolute;
        right: 0;
        top: 100%;
        transform: scaleX(0);
        transform-origin: right;
        transition: transform .5s cubic-bezier(.895,.03,.685,.22)
    }

    .Contact .Map-infoWindow {
        padding: 1vh 1vw
    }

    .Contact .Map-infoWindow-title {
        font-weight: 500
    }

    .Contact .Map div:not([class]) {
        overflow: visible!important;
        overflow: initial!important
    }

    .Legal {
        background: #111;
        color: #fff;
        display: flex;
        flex-direction: column;
        min-height: 100vh
    }

    .Legal-inner {
        padding: 10vh 7.6vw 6vh
    }

    @media(max-width: 992px) {
        .Legal-inner {
            padding-top:16vh
        }
    }

    @media(min-width: 577px) {
        .Legal-inner {
            margin:auto
        }
    }

    .Legal-row {
        grid-gap: 20px 60px;
        display: grid
    }

    @media(min-width: 577px) {
        .Legal-row {
            grid-template:max-content/repeat(2,max-content)
        }

        .Legal-row>:first-child {
            grid-row: span 2
        }
    }

    .Projects {
        align-items: center;
        display: flex;
        justify-content: center;
        min-height: 100vh;
        overflow: hidden
    }

    .Projects-layoutBtns {
        background-color: #000;
        bottom: 0;
        color: #fff;
        display: flex;
        gap: 12px;
        height: 50px;
        padding: 20px;
        position: fixed;
        right: 280px;
        transition: transform .7s cubic-bezier(.23,1,.32,1)
    }

    .Projects-layoutBtns.is-hidden {
        transform: translateY(100%)
    }

    @media(max-width: 1200px) {
        .Projects-layoutBtns {
            transform:translateY(100%);
            transition-timing-function: cubic-bezier(.86,0,.07,1)
        }
    }

    .Projects-layoutBtn {
        cursor: pointer;
        opacity: .2;
        transition: opacity .3s linear
    }

    .Projects-layoutBtn.is-active,.Projects-layoutBtn:hover {
        opacity: 1
    }

    .Projects-layoutBtn.is-active {
        pointer-events: none
    }

    [class*=page-projects-slug].is-down .Header {
        transform: translateY(-100%)
    }

    [class*=page-projects-slug] .Header {
        transition: transform 1s cubic-bezier(.77,0,.175,1)
    }

    .Project {
        background-color: #fff
    }

    @media(max-width: 767px) {
        .Project {
            gap:0;
            padding-top: 0
        }
    }

    .Project.is-going-to-projects:after {
        transform: scaleY(1)
    }

    .Project:after {
        background-color: #111;
        bottom: 0;
        content: "";
        display: block;
        left: 0;
        position: fixed;
        right: 0;
        top: 0;
        transform: scaleY(0);
        transform-origin: bottom;
        transition: transform 1s cubic-bezier(1,0,0,1);
        z-index: 10
    }

    .Project-backArea {
        align-items: center;
        background-color: hsla(0,0%,7%,.5);
        display: flex;
        padding-bottom: 40px;
        padding-top: 40px;
        position: fixed;
        transition: opacity 1s cubic-bezier(.23,1,.32,1) .8s,transform 1s cubic-bezier(.77,0,.175,1);
        width: 100%;
        z-index: 2
    }

    body:not(.is-loaded) .Project-backArea {
        opacity: 1;
    }

    .is-down .Project-backArea {
        transform: translateY(-100%)
    }

    @media(min-width: 577px) {
        .Project-backArea {
            padding-bottom:40px;
            padding-top: 40px
        }
    }

    @media(max-width: 576px) {
        .Project-backArea {
            padding-bottom:30px;
            padding-top: 30px
        }
    }

    .Project-backIcon {
        color: #fff;
        cursor: pointer;
        opacity: 1;
        transform: rotate(-90deg) translateY(50px);
        transition: transform 1s cubic-bezier(.23,1,.32,1) .8s
    }

    .is-loaded .Project-backIcon {
        opacity: 1;
        transform: rotate(-90deg) translateY(0)
    }

    .Project-hero {
        background-color: #111;
        color: #fff;
        height: var(--hero-height);
        position: relative
    }

    .Project-heroContent {
        z-index: 1
    }

    .Project-heroName {
        display: inline-block;
        font-size: 4.375rem;
        letter-spacing: -.02em;
        overflow: hidden;
        position: relative
    }

    .Project-heroName>* {
        display: block;
        transition: transform 1s cubic-bezier(.19,1,.22,1)
    }

    @media(max-width: 1440px) {
        .Project-heroName {
            font-size:2rem
        }
    }

    .Project-heroInfos>*,body:not(.is-loaded) .Project-heroName>* {
        transform: translateY(100%)
    }

    .Project-heroInfos>* {
        opacity: 1;
        transition: transform .8s cubic-bezier(.23,1,.32,1),opacity .5s cubic-bezier(.23,1,.32,1)
    }

    .is-loaded .Project-heroInfos>:first-child {
        opacity: 1;
        transform: none;
        transition-delay: .12s,.12s
    }

    .is-loaded .Project-heroInfos>:nth-child(2) {
        opacity: 1;
        transform: none;
        transition-delay: .17s,.17s
    }

    .is-loaded .Project-heroInfos>:nth-child(3) {
        opacity: 1;
        transform: none;
        transition-delay: .22s,.22s
    }

    .is-loaded .Project-heroInfos>:nth-child(4) {
        opacity: 1;
        transform: none;
        transition-delay: .27s,.27s
    }

    .is-loaded .Project-heroInfos>:nth-child(5) {
        opacity: 1;
        transform: none;
        transition-delay: .32s,.32s
    }

    .is-loaded .Project-heroInfos>:nth-child(6) {
        opacity: 1;
        transform: none;
        transition-delay: .37s,.37s
    }

    .is-loaded .Project-heroInfos>:nth-child(7) {
        opacity: 1;
        transform: none;
        transition-delay: .42s,.42s
    }

    .is-loaded .Project-heroInfos>:nth-child(8) {
        opacity: 1;
        transform: none;
        transition-delay: .47s,.47s
    }

    .is-loaded .Project-heroInfos>:nth-child(9) {
        opacity: 1;
        transform: none;
        transition-delay: .52s,.52s
    }

    .is-loaded .Project-heroInfos>:nth-child(10) {
        opacity: 1;
        transform: none;
        transition-delay: .57s,.57s
    }

    .Project-section--color1 {
        background-color: #0b2819;
        color: #fff
    }

    .Project-section--color1 .Project-sectionDetails {
        color: #fff
    }

    .Project-section--color1 .Project-sectionDetails:first-line,.Project-section--color1 .Project-title {
        color: #1efd8d
    }

    .Project-section--color2 {
        background-color: #111;
        color: #fff
    }

    .Project-section--color3 {
        background-color: #f4f4f4
    }

    .Project-section--topLabel .Project-sectionInner {
        align-items: flex-start
    }

    .Project-section--topLabel .Project-label--floating {
        margin-top: 7px
    }

    .Project-section--gallery {
        margin-top: 170px
    }

    .Project-sectionInner {
        align-items: flex-end;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        margin: 0 auto;
        max-width: 1240px;
        padding: 100px 120px;
        width: 100%
    }

    @media(max-width: 1400px) {
        .Project-sectionInner {
            padding-left:190px
        }
    }

    @media(max-width: 992px) {
        .Project-sectionInner {
            align-items:flex-start;
            flex-direction: column;
            padding: 70px 8.6vw
        }
    }

    .Project-sectionBorder {
        background-color: hsla(0,0%,7%,.2);
        height: 1px;
        width: 100%
    }

    @media(min-width: 993px) {
        .Project-sectionBorder {
            margin:0 0 -100px
        }
    }

    @media(max-width: 992px) {
        .Project-sectionBorder {
            margin:70px 0 -70px
        }
    }

    .Project-sectionDetails {
        color: hsla(0,0%,7%,.5);
        font-size: .875rem;
        line-height: 1.3
    }

    .Project-sectionDetails:first-line {
        color: #111
    }

    @media(min-width: 993px) {
        .Project-sectionDetails {
            text-align:right
        }
    }

    .Project-sectionDetails a {
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .Project-sectionDetailsList {
        color: #111;
        display: grid
    }

    .Project-sectionDetailsList,.Project-sectionDetailsList .Project-label {
        font-size: .875rem
    }

    @media(max-width: 1440px) {
        .Project-sectionDetailsList,.Project-sectionDetailsList .Project-label {
            font-size:1rem
        }
    }

    @media(min-width: 768px) {
        .Project-sectionDetailsList {
            gap:10px
        }
    }

    @media(max-width: 767px) {
        .Project-sectionDetailsList {
            gap:20px
        }
    }

    .Project-sectionDetailsListItem {
        grid-gap: 20px;
        display: grid;
        gap: 20px
    }

    @media(min-width: 768px) {
        .Project-sectionDetailsListItem {
            grid-template-columns:150px 1fr
        }
    }

    @media(max-width: 767px) {
        .Project-sectionDetailsListItem {
            gap:5px
        }
    }

    .Project-sectionDetailsLink {
        -webkit-text-decoration: underline;
        text-decoration: underline
    }

    .Project-title {
        font-size: 3.125rem;
        line-height: 1
    }

    @media(max-width: 992px) {
        .Project-title {
            margin-bottom:50px
        }
    }

    @media(max-width: 576px) {
        .Project-title small {
            font-size:1.25rem
        }
    }

    .Project-label {
        font-size: .875rem;
        opacity: .5
    }

    @media(min-width: 993px) {
        .Project-label--floating {
            left:40px;
            margin-bottom: 4px;
            position: absolute
        }
    }

    @media(max-width: 992px) {
        .Project-label--floating {
            margin-bottom:10px
        }
    }

    .Project-links {
        grid-gap: 40px;
        display: grid;
        gap: 40px;
        grid-auto-flow: column;
        padding-bottom: 4px
    }

    .Project-link {
        grid-gap: 20px;
        color: currentColor;
        display: grid;
        gap: 20px;
        grid-auto-flow: column
    }

    .Project-typeIcon {
        height: 29px
    }

    .Project-description .Project-sectionDetails {
        text-align: left
    }

    @media(max-width: 1440px) {
        .Project-description .Project-sectionDetails {
            width:auto
        }
    }

    .Project-descriptionParagraph {
        font-size: 1.25rem;
        letter-spacing: -.005em;
        line-height: 1.3
    }

    @media(min-width: 1441px) {
        .Project-descriptionParagraph {
            max-width:400px
        }
    }

    @media(max-width: 1440px) {
        .Project-descriptionParagraph {
            margin-bottom:35px
        }
    }

    @media(min-width: 1441px) {
        .Project-gallery,.Project-nextProject {
            margin-top:130px
        }

        .Project-gallery+.Project-gallery,.Project-gallery+.Project-nextProject,.Project-nextProject+.Project-gallery,.Project-nextProject+.Project-nextProject {
            margin-top: 0
        }
    }

    @media(max-width: 1440px) {
        .Project-plans .Project-sectionInner {
            padding-top:50px
        }
    }

    .Project-plansList {
        display: grid
    }

    .Project-nextProject .Project-sectionInner {
        max-width: none
    }

    @media(min-width: 1441px) {
        .Project-nextProject .Project-sectionInner {
            padding-left:240px;
            padding-right: 8.6vw
        }
    }

    @media(max-width: 767px) {
        .Project-nextProject .Project-sectionInner {
            padding-bottom:0;
            padding-left: 0;
            padding-right: 0
        }

        .Project-nextProject .Project-sectionInner .Project-label {
            padding-left: 8.6vw;
            padding-right: 8.6vw
        }
    }

    @media(min-width: 1441px) {
        .Project-nextProject .Project-sectionInner .ProjectCard-name {
            font-size:1.875rem
        }
    }

    .Project-nextProject .Project-sectionCards {
        grid-gap: 10px;
        display: grid;
        gap: 10px;
        width: 100%
    }

    @media(min-width: 993px) {
        .Project-nextProject .Project-sectionCards {
            grid-template:repeat(2,1fr)/repeat(2,1fr)
        }
    }

    @media(max-width: 992px) {
        .Project-nextProject .Project-sectionCards {
            gap:8px;
            padding: 8px
        }
    }

    .Project-nextProject .Project-sectionCardsItem {
        perspective: 1500px
    }

    .News {
        color: #fff
    }

    .nuxt-progress {
        background-color: #000;
        height: 2px;
        left: 0;
        opacity: 1;
        position: fixed;
        right: 0;
        top: 0;
        transition: width .1s,opacity .4s;
        width: 0;
        z-index: 999999
    }

    .nuxt-progress.nuxt-progress-notransition {
        transition: none
    }

    .nuxt-progress-failed {
        background-color: red
    }
</style>

</style>