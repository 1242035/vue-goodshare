<template>
  <div>
    <div v-if="this.$props.bundle === 'world'">
      <vue-goodshare-facebook has_icon has_counter title_social="Facebook"/>
      <vue-goodshare-twitter has_icon title_social="Twitter"/>
      <vue-goodshare-email has_icon title_social="Email"/>
    </div>
    <div v-if="this.$props.bundle === 'ru'">
      <vue-goodshare-facebook has_icon has_counter title_social="Фейсбук"/>
      <vue-goodshare-twitter has_icon title_social="Твиттер"/>
      <vue-goodshare-email has_icon title_social="Электронная почта"/>
    </div>
    <div v-if="this.$props.bundle === 'mobile'">
      <vue-goodshare-telegram has_icon title_social="Telegram"/>
      <vue-goodshare-viber has_icon title_social="Viber"/>
      <vue-goodshare-whats-app has_icon title_social="WhatsApp"/>
      <vue-goodshare-line has_icon title_social="LINE"/>
    </div>
  </div>
</template>

<script>
// Import VueGoodshare social network components
//import VueGoodshareVkontakte from "./providers/Vkontakte.vue";
//import VueGoodshareOdnoklassniki from "./providers/Odnoklassniki.vue";
import VueGoodshareFacebook from "./providers/Facebook.vue";
//import VueGoodshareMoiMir from "./providers/MoiMir.vue";
import VueGoodshareTwitter from "./providers/Twitter.vue";
//import VueGoodshareLiveJournal from "./providers/LiveJournal.vue";
//import VueGoodshareLinkedIn from "./providers/LinkedIn.vue";
//import VueGoodshareTumblr from "./providers/Tumblr.vue";
//import VueGoodsharePinterest from "./providers/Pinterest.vue";
//import VueGoodshareReddit from "./providers/Reddit.vue";

// Import VueGoodshare mobile messenger components
import VueGoodshareTelegram from "./providers/Telegram.vue";
import VueGoodshareViber from "./providers/Viber.vue";
import VueGoodshareWhatsApp from "./providers/WhatsApp.vue";
import VueGoodshareLine from "./providers/Line.vue";

// Import VueGoodshare misc components
import VueGoodshareEmail from "./providers/Email.vue";

export default {
  name: "VueGoodshare",
  props: {
    bundle: {
      type: String,
      default: "world"
    }
  },
  components: {
    //VueGoodshareVkontakte,
    //VueGoodshareOdnoklassniki,
    VueGoodshareFacebook,
    //VueGoodshareMoiMir,
    //VueGoodshareLiveJournal,
    //VueGoodshareLinkedIn,
    //VueGoodshareTumblr,
    //VueGoodsharePinterest,
    //VueGoodshareReddit,
    VueGoodshareTwitter,
    VueGoodshareTelegram,
    VueGoodshareViber,
    VueGoodshareWhatsApp,
    VueGoodshareLine,
    VueGoodshareEmail
  }
};
</script>
