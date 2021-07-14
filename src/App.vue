<template>
  <div>
    <div>
      <h1>{{ head }}</h1>
      <br>
      <button class="btn" v-on:click="generate()">Ideas</button>
    </div>

    <div class="footer">
      Made with ❤️, built with vue<br>
      Source code is available on <a href="https://github.com/Sidhhh/app-idea-generator">Github</a>
    </div>

  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      head: (
        '/*IDEAS*/'
      ),
      app: [
        'pintrest',
        'tik Tok',
        'netflix',
        'faceBook',
        'gmail',
        'strava',
        'github',
        'spotify',
        'duolingo',
        'uber',
        'pastemyst',
        'ebay',
        'youtube',
        'snapchat',
        'gitlab',
        'trello',
        'notion',
        'audacity',
        'instagram',
        'twitch',
        'google Play',  
        'cred',
      ],
      audience: [
        'gamers',
        'artists',
        'writers',
        'chefs',
        'nerds',
        'eating',
        'watching movie',
        'vloggers',
        'scientists',
        'bloggers',
        'memes',
        'birds',
        'cats',
        'dogs'
      ]
    }
  },
  methods: {
    generate() {
      let app =  this.app[Math.trunc(Math.random() * this.app.length)]
      let audience =  this.audience[Math.trunc(Math.random() * this.audience.length)]

      if (
        app.startsWith('a')||
        app.startsWith('e')||
        app.startsWith('i')||
        app.startsWith('o')||
        app.startsWith('u')
        ) {
        this.head = `An ${app} for ${audience}.`
      } else {
        this.head = `A ${app} for ${audience}.`
      }
  
    }
  },

};
</script>

<style>
@import "./styles/app.css";
</style>
