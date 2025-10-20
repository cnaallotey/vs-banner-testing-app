<script setup>

const affiliate = ref('vueschool_free')
const { data, error } = await useAsyncData('banner-data', async () => {
  try {
    const response = await $fetch(`https://staging-banner.bitterbrains.com/json/${affiliate.value}`)
    return response
  } catch (err) {
    console.error('Banner API error:', err)
    throw err
  }
})

const banner =  {
      "id": "AIDD_WORKSHOP-OCT_REGISTRATION_AFFILIATES",
      "ends": "2025-10-22T14:59:59.000000Z",
      "affiliates": [
        "vueuse",
        "pinia",
        "vuerouter",
        "vueschool",
        "vueschool_free",
        "vueschool_premium",
        "vuejsdevelopers",
        "vuejsnation",
        "nuxtnation",
        "vuejsforge",
        "LEARNVUE",
        "masteringnuxt",
        "vs_frontendnation",
        "vs_masteringpinia",
        "ANGADEMY",
        "UILIB",
        "VUEMASTERY",
        "ANGUNI",
        "DOTNET",
        "NSCRIPT",
        "angulartraining"
      ],
      "cta": "Register now",
      "link": "https://aidd.io/workshop",
      "title": "Ship <span>20x Faster<\/span> with AI",
      "assets": "AIDD_LAUNCH",
      "static": "AIDD_WORKSHOP_REGISTRATION",
      "classes": [
        "bb-campaign-aidd-workshop"
      ],
      "prelude": " ",
      "addendum": null,
      "ctaOffer": null,
      "internal": false,
      "subtitle": "Join a <b>free workshop</b> to explore LLMs and advanced AI tools.",
      "offerLink": null,
      "showCountdown": true,
      "countdownFooter": "Ends in",
      "showDaysAsHours": false,
      "affiliatesWithCountdown": null
    }

</script>
<template>
  <div>
    <div id="bb-banner-container" class="card" data-v-71c3ef53="">
      <a
        id="bb-banner"
        target="_blank"
        href="https://vueschool.io/sales/vuejsamsterdam24?utm_source=vuejsforge&amp;utm_medium=website&amp;utm_campaign=affiliate&amp;utm_content=inline_banner&amp;banner_type=inline&amp;friend=VUEJSFORGE"
        class="bb-campaign-vs-test"
      >
        <div class="bb-background"></div>
        <div class="bb-logo"></div>
        <div class="bb-side-image"></div>
        <div class="bb-core">
          <div class="bb-slogan">
            <div v-if="banner.prelude" class="bb-prelude" v-html="banner.prelude"></div>
            <div class="bb-title-container">
              <div v-if="banner.title" class="bb-title" v-html="banner.title">
              
              </div>
              <div v-if="banner.subtitle" class="bb-subtitle" v-html="banner.subtitle">
              </div>
            </div>
            <div v-if="banner.interlude" class="bb-interlude" v-html="banner.interlude"></div>
          </div>
          <div v-if="banner.cta" class="bb-button-wrapper"><div class="bb-button">{{ banner.cta }}</div></div>
          <div class="bb-countdown-container">
            <div v-if="banner.addendum" class="bb-addendum">{{ banner.addendum }}</div>
            <div v-if="banner.showCountdown" class="bb-countdown-wrapper">
              <div v-if="banner.countdownFooter" class="bb-countdown-footer">{{ banner.countdownFooter }}</div>
              <div class="bb-countdown">
                <div class="bb-countdown-item">
                  <div class="bb-countdown-part">
                    <div data-countdown="hours" class="bb-countdown-number">07</div>
                    <div class="bb-countdown-text">
                      <span class="bb-countdown-text-initial">h</span
                      ><span class="bb-countdown-text-rest">ours</span>
                    </div>
                  </div>
                  <div class="bb-countdown-colon">:</div>
                </div>

                <div class="bb-countdown-item">
                  <div class="bb-countdown-part">
                    <div data-countdown="minutes" class="bb-countdown-number">28</div>
                    <div class="bb-countdown-text">
                      <span class="bb-countdown-text-initial">m</span
                      ><span class="bb-countdown-text-rest">inutes</span>
                    </div>
                  </div>
                  <div class="bb-countdown-colon">:</div>
                </div>

                <div class="bb-countdown-item">
                  <div class="bb-countdown-part">
                    <div data-countdown="seconds" class="bb-countdown-number">27</div>
                    <div class="bb-countdown-text">
                      <span class="bb-countdown-text-initial">s</span
                      ><span class="bb-countdown-text-rest">econds</span>
                    </div>
                  </div>
                  <div class="bb-countdown-colon">:</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div id="bb-close" class="bb-close">
          <svg
            width="14"
            height="14"
            viewBox="0 0 14 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M13.6894 0.321198C13.2753 -0.0929086 12.6064 -0.0929086 12.1923 0.321198L7 5.50284L1.80774 0.31058C1.39363 -0.103527 0.724687 -0.103527 0.31058 0.31058C-0.103527 0.724687 -0.103527 1.39363 0.31058 1.80774L5.50284 7L0.31058 12.1923C-0.103527 12.6064 -0.103527 13.2753 0.31058 13.6894C0.724687 14.1035 1.39363 14.1035 1.80774 13.6894L7 8.49716L12.1923 13.6894C12.6064 14.1035 13.2753 14.1035 13.6894 13.6894C14.1035 13.2753 14.1035 12.6064 13.6894 12.1923L8.49716 7L13.6894 1.80774C14.0929 1.40425 14.0929 0.724687 13.6894 0.321198Z"
              fill="white"
            ></path>
          </svg>
        </div>
      </a>
    </div>
  </div>
</template>

<style>
@import url("~/assets/css/test.css");
</style>