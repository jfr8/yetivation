<template>
  <the-header></the-header>
  <data-store :records="recordsCollection"></data-store>
  <the-footer></the-footer>
</template>

<script>
import DataStore from "./components/DataStore.vue";
import TheHeader from "./components/UI/TheHeader.vue";
import TheFooter from "./components/UI/TheFooter.vue";

export default {
  components: {
    DataStore,
    TheHeader,
    TheFooter,
  },
  data() {
    return {
      recordsCollection: [
        {
          id: "Record0",
          title: "The College Dropout",
          quote: [
            '"It seems we living the American dream, But the people highest up got the lowest self-esteem & prettiest people do the ugliest things"',
            '"For the road to riches and diamond rings, We shine because they hate us, floss cause they degrade us, we trynna buy back our 40 acres"',
            "Two words, United States, no love, no breaks / Low brow, high stakes, crack smoke, black folks",
          ],
          link: "https://sample.com",
          image: "collegeDropout.png",
        },
        {
          id: "Record1",
          title: "Late Registration",
          quote: [
            '"They say people in your life for seasons/And anything that happen is for a reason"',
            '"There will always be haters, thats the way it is/Hater niggas marry hater bitches and have hater kids"',
            '"Whats your addiction? Is it money? Is it girls? Is it weed? Ive been afflicted by not one, not two, but all three"',
          ],
          link: "https://sample2.com",
          image: "lateRegistration.png",
        },
        {
          id: "Record2",
          title: "Graduation",
          quote: [
            '"Everything Im not made me everything I am"',
            '"You ever wonder what it all really means? You ever wonder if youd find your dream?"',
            '"She dont believe in shooting starts, but she believe in shoes and cars.."',
          ],
          link: "https://sample2.com",
          image: "graduation.png",
        },
        {
          id: "Record3",
          title: "808s and heartbreak",
          quote: [
            '“I wish this song would really come true. I admit I still fantasize about you."',
            "“You wait a couple months, then you gon’ see, you’ll never find nobody better than me.”",
            "“Why would she make calls out the blue? Now I’m awake, sleepless in you.”",
          ],
          image: "808s.png",
        },
        {
          id: "Record4",
          title: "My Beautiful Dark Twisted Fantasy",
          quote: [
            "You're my devil, you're my angel, You're my heaven, you're my hell, You're my now, you're my forever",
            "If we die in each other's arms, still get laid in the afterlife.",
            "I'm making love to the angel of death/Catching feelings never stumble, retracing my steps",
          ],
          image: "mbdtf.png",
        },
        {
          id: "Record5",
          title: "Yeezus",
          quote: ["Old niggas mentally still in high school", 
          "You see there’s leaders and there’s followers But I’d rather be a dick than a swallower",
        "We could’ve been somebody ‘stead you had to tell somebody"],
          image: "yeezus.png",
        },
        {
          id: "Record6",
          title: "The Life Of Pablo",
          quote: ["Waves don't die", "You are the sun in my morning babe, nothing unwanted" , "This is a God dream, this is everything."],
          image: "pablo.png",
        },
        {
          id: "Record7",
          title: "Ye",
          quote: ["Im on 1,2,3,4,5 no half truths just naked minds, caught between space and time", "You might think they wrote you off, they gon have to rope me off",
        "They been tryna test my Ghandi, just because im dressed like abercrombie"],
          image: "ye.png",
        },
        {
          id: "Record8",
          title: "Jesus Is King",
          quote: ["All my idols, let em go, all the demons, let em know, this a mission not a show", "I bow down to the King upon the throne", "My life is His, Im no longer on my own"],
          image: "jesus.png",
        },
        {
          id: "Record9",
          title: "Donda",
          quote: ["Made in the image of God, thats a selfie", "Better find God before he find me, tell the devil good nit, go to sleep", "I wanna go to the moon, dont leave so soon, how can i get thru?"],
          image: "donda.png",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}
</style>