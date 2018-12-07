<template>
  <v-app dark>
    <v-toolbar>
      <v-toolbar-title>BladeNEXT</v-toolbar-title>
    </v-toolbar>
    <v-content>
      <nuxt />
    </v-content>
    <v-footer 
      dark 
      height="auto">
      <v-card 
        class="text-xs-center">
        <v-card-text>
          <v-btn
            v-for="(item, i) in items"
            :to="item.to"
            :key="i"
            icon
            class="mx-3 white--text"
          >
            <v-icon size="24px">{{ item.icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <v-card-text class="white--text pt-0">
          Klasaとdiscord.jsを利用した最高のボット(?)、多機能目指して制作しています。困った事などがあればDiscordへ参加して気軽に聞いて下さい;) BladeNEXTをより良いボットに成長させるにはあなたの協力が必要です。
        </v-card-text>
        <v-divider/>
        <v-card-text class="white--text">
          &copy;2018 — <strong>DJS-JPN Unoffical</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { icon: 'home', to: '/' },
        { icon: 'textsms', to: 'https://discord.gg/DbTpjXV' },
        { icon: 'label', to: 'https://github.com/DJS-JPN/Blade-NEXT/releases' }
      ]
    }
  }
}
</script>
