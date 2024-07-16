<template>
  <div class="sidenav-container">
    <div
      v-if="show"
      class="sidenav-backdrop"
      @click="$emit('close')">
    </div>
    <transition name="slide-side">
      <div
      v-if="show"
      class="sidenav">
      <nav class="Menu-nav">
        <ul
        class="nav-list"
        @click="$emit('close')">
          <li>
            <a href="/" aria-current="page" class="Menu-link nuxt-link-exact-active nuxt-link-active">Home</a>
          </li> 
          <li>
            <a href="/agriculture" class="Menu-link">Agriculture</a>
          </li> 
          <li>
            <a href="/algae" class="Menu-link">Algae</a>
          </li> 
          <li>
            <a href="/industrials" class="Menu-link">Industrials</a>
          </li> 
          <li>
            <a href="/partnerships" class="Menu-link">Partnerships</a>
          </li>
          <li>
            <a href="/contact" class="Menu-link">Contact</a>
          </li>
        </ul>
      </nav> 
      <div class="LangSwitcher Menu-langSwitcher">
        <div class="LangSwitcher-item">
          <a href="/" aria-current="page" class="LangSwitcher-link nuxt-link-exact-active nuxt-link-active">English</a>
        </div>
        <div class="LangSwitcher-item">
          <a href="/fr" class="LangSwitcher-link">Swahili</a>
        </div>
      </div>
      <div class="Menu-aside">
      <a href="/news" class="Menu-link Menu-title">News</a> 
      <div class="Menu-newsList">
        <article class="Menu-newsCard">
          <figure class="Menu-newsCardFigure">
            <img alt="LEKO rewarded as best European Protech" class="u-mediaCover is-lazy is-loaded" src="//images.ctfassets.net/fmhnbftl7a81/39eK5LgR2IwwJgvkvrtiAA/0d2f467d0c1e5df731e6aa2e9f451a41/Capture_d__cran_2023-10-18___17.43.29.jpg">
          </figure>
          <span class="Menu-newsCardTitle">Coastal Biotech awarded as best European PropTech</span>
          <a href="https://www.proptechhouse.eu/leko-labs-wins-european-proptech-association-startup-scaleup-award-2023/" rel="noopener noreferrer" target="_blank" class="Menu-newsCardLink"></a>
        </article>
        <article class="Menu-newsCard">
          <figure class="Menu-newsCardFigure">
            <img alt="Paperjam.lu 50- leaders 2" class="u-mediaCover is-lazy is-loaded" src="//images.ctfassets.net/fmhnbftl7a81/3yWHSai1aJ8yYTQXLTkWhR/9ef9429e1c5589bf386956a63aebed40/Paperjam.lu_50-_leaders_2.jpg">
          </figure>
          <span class="Menu-newsCardTitle">Our founder, in the 50 leaders of Luxembourg's tech industry</span>
          <a href="https://paperjam.lu/article/who-s-who-in-tech-2021" rel="noopener noreferrer" target="_blank" class="Menu-newsCardLink"></a>
        </article>
      </div> 
      <a href="/news" class="Menu-newsMore">More<svg width="20" height="20" class="Menu-newsMoreIcon"><use xlink:href="/sprite.svg#arrow"></use></svg></a> 
      <form class="SubscribeForm">
        <label class="SubscribeForm-label Paragraph Paragraph--smaller">Stay up to date on all the LEKO news!</label> 
        <div class="SubscribeForm-fields">
          <input type="email" pattern="[a-zA-Z0-9._-]+@[a-zA-Z0-9._-]+.[a-zA-Z.]{2,15}" placeholder="Email" class="SubscribeForm-input"> 
          <button type="submit" class="SubscribeForm-submit">
            <span class="u-relative">Subscribe</span>
          </button> 
          <span class="SubscribeForm-status"></span> <!----> <!---->
        </div>
      </form>
    </div> 
    <div class="Menu-backdrop"></div>
    </div>
    
        
    </transition>
  </div>
</template>

<script>
export default {
  name: "TheSidenav",
  props: {
    show: {
      type: Boolean,
      default: false
    }
  }
};
</script>


<style scoped>
.sidenav-container {
  height: 100%;
  width: 100%;
}

.sidenav-backdrop {
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 1000;
  position: fixed;
  top: 0;
  left: 0;
}

.sidenav {
  height: 100%;
  width: 500px;
  background-color: white;
  z-index: 10000;
  position: fixed;
  top: 0;
  left: 0;
  box-sizing: border-box;
  padding: 30px;
}

.slide-side-enter-active,
.slide-side-leave-active {
  transition: all 0.3s ease-out;
}
.slide-side-enter,
.slide-side-leave-to {
  transform: translateX(-100%);
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  margin: 20px 0;
}

.nav-item a {
  text-decoration: none;
  color: black;
  font-size: 1.5rem;
}

.nav-item a:hover,
.nav-item a:active {
  color: red;
}
</style>
