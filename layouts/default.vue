<template>
  <div>
    <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
    <TheSidenav
      :show="displaySidenav"
      @close="displaySidenav=false"></TheSidenav>
    <nuxt/>
  </div>
</template>

<script type="text/javascript">
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'

export default {
  components: {
    TheHeader,
    TheSidenav
  },
  data() {
    return {
      displaySidenav: false
    }
  },
  mounted() {
    let self = this;
    window.addEventListener('keyup', function(event) {
      if (event.key == "Escape") {
        self.displaySidenav = false
      }
    })
  }
}
</script>

<style>
html {
  font-family: 'Oswald', sans-serif;
}

body {
  margin: 0;
}
</style>
