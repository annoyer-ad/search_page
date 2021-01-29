<template>
  <q-layout view="hHh LpR fFf">

    <q-header reveal height-hint="98" class="bg-grey-1 text-black">
      <q-tabs align="right" style="padding:0;">
        <q-route-tab to="/page1" label="Gmail" style="padding:0;"/>
        <q-route-tab to="/page2" label="Images" style="padding:0;"/>
        <q-img
          src="../assets/iconsquare.png"
          width="35px"
          height="28px"
          style="margin:0 2%;"
          role="button"
        />
        <q-btn
          color="primary"
          label="Sign In"
          padding="sm md"
          style="margin:1% 2% 1% 0;padding-right:2%;"
        />
      </q-tabs>
    </q-header>

    <q-page-container align="center" style="margin-top:5%;padding:8%;">
      <q-img
          alt="Google" height="92px" src="../assets/google.png" width="272px"
      />
     <q-tabs align="center" style="margin:4%;">
     <q-btn color="white" class="text-grey-7" label="Google Search" style="margin:1%;padding-right:2%;border:none;" />
     <q-btn color="white" class="text-grey-7" label="I'm feeling lucky" style="margin:1%;padding-right:2%;border:none;" />
     </q-tabs>
      <router-view />
    </q-page-container>
    <q-footer reveal class="bg-grey-3 text-grey-7">
      <q-tabs align="left" reveal class="bg-grey-3 text-grey-7">
        <q-route-tab to="/page1" label="France" />
      </q-tabs>
      <q-tabs align="left">
        <q-route-tab to="/page1" label="Advertising" />
        <q-route-tab to="/page2" label="Business" />
        <q-route-tab to="/page3" label="About" />
        <q-route-tab to="/page3" label="How search works" />
      </q-tabs>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      search: ''
    }
  }
}
</script>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
<style>
.q-btn__wrapper:before {
    box-shadow: none;
}
.q-btn--actionable.q-btn--standard .q-btn__wrapper:before {
    transition: none;
}
</style>
