<script setup>
import TheHeader from './components/TheHeader.vue';
import SocialMediaCard from './components/SocialMediaCard.vue';
import OverviewCard from './components/OverviewCard.vue';
import TheCredits from './components/TheCredits.vue';
</script>

<template>
  <TheHeader />

  <main>
    <section class="top-section">
      <SocialMediaCard 
        class="facebook-card"
        socialIcon="/images/icon-facebook.svg"
        socialUser="@nathanf"
        socialTotal="1987"
        of="Followers"
        arrowIcon="/images/icon-up.svg"
        totalToday="12"
      />
      <SocialMediaCard
        class="twitter-card" 
        socialIcon="/images/icon-twitter.svg"
        socialUser="@nathanf"
        socialTotal="1044"
        of="Followers"
        arrowIcon="/images/icon-up.svg"
        totalToday="99"
      />
      <div class="instagram-card-border">
        <SocialMediaCard
        class="instagram-card"
        socialIcon="/images/icon-instagram.svg"
        socialUser="@realnathanf"
        socialTotal="11k"
        of="Followers"
        arrowIcon="/images/icon-up.svg"
        totalToday="1099"
      />
      </div>
      <SocialMediaCard
        class="youtube-card" 
        socialIcon="/images/icon-youtube.svg"
        socialUser="Nathan F."
        socialTotal="8239"
        of="Subscribers"
        arrowIcon="/images/icon-down.svg"
        totalToday="144"
      />
    </section>

    <h3>Overview - Today</h3>

    <section class="bottom-section">
      <OverviewCard
        socialEngagement="Page Views"
        socialTotal="87"
        socialIcon="/images/icon-facebook.svg"
        arrowIcon="/images/icon-up.svg"
        totalToday="3%"
      />
      <OverviewCard
        class="down"
        socialEngagement="Likes"
        socialTotal="52"
        socialIcon="/images/icon-facebook.svg"
        arrowIcon="/images/icon-down.svg"
        totalToday="2%"
      />
      <OverviewCard
        socialEngagement="Likes"
        socialTotal="5462"
        socialIcon="/images/icon-instagram.svg"
        arrowIcon="/images/icon-up.svg"
        totalToday="2257%"
      />
      <OverviewCard
        socialEngagement="Profile Views"
        socialTotal="52k"
        socialIcon="/images/icon-instagram.svg"
        arrowIcon="/images/icon-up.svg"
        totalToday="1375%"
      />
      <OverviewCard
        socialEngagement="Retweets"
        socialTotal="117"
        socialIcon="/images/icon-twitter.svg"
        arrowIcon="/images/icon-up.svg"
        totalToday="303%"
      />
      <OverviewCard
        socialEngagement="Likes"
        socialTotal="507"
        socialIcon="/images/icon-twitter.svg"
        arrowIcon="/images/icon-up.svg"
        totalToday="553%"
      />
      <OverviewCard
        class="down"
        socialEngagement="Likes"
        socialTotal="107"
        socialIcon="/images/icon-youtube.svg"
        arrowIcon="/images/icon-down.svg"
        totalToday="19%"
      />
      <OverviewCard
        class="down"
        socialEngagement="Total Views"
        socialTotal="1407"
        socialIcon="/images/icon-youtube.svg"
        arrowIcon="/images/icon-down.svg"
        totalToday="12%"
      />
    </section>
  </main>
  <TheCredits 
    link-frontend-mentor="https://www.frontendmentor.io/challenges/social-media-dashboard-with-theme-switcher-6oY8ozp_H"
    link-github="https://github.com/VickyAzola/SocialMeidaDashboard-ThemeSwitch"
  />
</template>

<style scoped>

main {
  margin: 0 2rem;
}
.facebook-card {
  border-top: 6px solid hsl(208, 92%, 53%);
}
.twitter-card {
  border-top: 6px solid hsl(203, 89%, 53%);
}
.instagram-card-border {
  width: 100%;
  background: linear-gradient(90deg, hsl(37, 97%, 70%), hsl(329, 70%, 58%));;
  padding-top: 8px;
  border-radius: .5rem;
  border-bottom: 1px solid hsl(227, 47%, 96%);
}
.instagram-card {
  margin: -2px 0;
  width: 100%;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
.youtube-card {
  border-top: 6px solid hsl(348, 97%, 39%);
}

.top-section {
  display: grid;
  gap: 1rem
}

h3 {
  font-size: 1.5rem;
  margin: 3rem 1.5rem 2rem; 
  color: var(--Text);
}

.bottom-section {
  display: grid;
  gap: 1rem
}

@media screen and (min-width: 600px) {

main {
  display: grid;
}
.top-section {
  margin-top: 1rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem
}

h3 {
  margin: 1.5rem; 
}

.bottom-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem
}

}


@media screen and (min-width: 1100px) {

  main {
    display: grid;
    place-content: center;
  }
  .top-section {
    margin-top: 1rem;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    column-gap: 1rem;
  }

  .instagram-card-border {
    margin: 0;
  }

  h3 {
    margin: 2rem 0 1rem 0; 
  }

  .bottom-section {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    column-gap: 1rem;
  }

}
</style>
