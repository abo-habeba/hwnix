<template>
  <v-container class="socials-container">
    <div>
      <v-row class="description-row ma-5">
        <v-col cols="12" class="description">
          <p class="description-text">
            مرحباً بك <br />
            يمكنك التواصل معنا من خلال قنوات التواصل الاجتماعي التالية. <br />
            لا تتردد في الاتصال بنا عبر أي من هذه القنوات:
          </p>
        </v-col>
      </v-row>
      <v-row class="socials-row ma-5">
        <v-col
          xs="6"
          sm="4"
          v-for="(social, i) in socials"
          :key="i"
          class="social-item"
        >
          <a
            :href="social.url"
            target="_blank"
            :title="social.name"
            class="social-link"
          >
            <span
              :style="{ color: social.color }"
              :class="['mdi', social.icon]"
            ></span>
          </a>
          <div class="social-description">
            {{ social.name }}
          </div>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script setup>
import { ref } from "vue";
// definePage({
//   meta: {
//     title: " تواصل معنا ",
//   },
// });
const socials = ref([
  {
    name: "Facebook",
    color: "blue",
    icon: "mdi-facebook",
    url: "https://www.facebook.com/hwnix",
  },
  {
    name: "Messenger",
    color: "blue",
    icon: "mdi-facebook-messenger",
    url: "https://m.me/hwnix",
  },
  {
    name: "WhatsApp",
    color: "green",
    icon: "mdi-whatsapp",
    url: "https://wa.me/+201021215988",
  },
  {
    name: "Call",
    color: "green",
    icon: "mdi-phone",
    url: "tel:01021215988",
  },
  {
    name: "Location",
    color: "red",
    icon: "mdi-map-marker",
    url: "https://maps.app.goo.gl/ka8PNiszWqn8yqKB6",
  },

  // {
  //   name: "Twitter",
  //   color: "skyblue",
  //   icon: "mdi-twitter",
  //   url: "https://www.twitter.com",
  // },
  // {
  //   name: "Instagram",
  //   color: "purple",
  //   icon: "mdi-instagram",
  //   url: "https://www.instagram.com",
  // },
  // {
  //   name: "YouTube",
  //   color: "red",
  //   icon: "mdi-youtube",
  //   url: "https://www.youtube.com",
  // },
  // {
  //   name: "TikTok",
  //   color: "black",
  //   icon: "mdi-tiktok",
  //   url: "https://www.tiktok.com",
  // },
]);
</script>

<style lang="scss" scoped>
.socials-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100vh;
  align-items: center;
  // gap: 20px;
}

.description-row {
  justify-content: center;
}

.description {
  text-align: center;
}

.description-text {
  font-size: 1rem;
  text-align: center;
  font-weight: bold;
}

.socials-row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
}

.social-item {
  text-align: center;
  transition: transform 0.3s;
}

.social-link {
  text-decoration: none;
  // color: inherit;
  // display: inline-flex;
  // align-items: center;
  // justify-content: center;
  // width: 50px;
  // height: 50px;
  // border-radius: 50%;
  // background-color: #f0f0f0;
  // padding: 10px;

  .mdi {
    font-size: 5rem !important;
  }
}

.social-link:hover .v-icon {
  transform: scale(1.3);
}

.social-description {
  font-size: 0.875rem;
  color: #333;
}
</style>
