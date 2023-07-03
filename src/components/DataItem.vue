<template>
  <li>
    <base-card class="base-card">
      <header>
        <h3>{{ title }}</h3>
      </header>

      <div class="card-body">
        <img
          :src="require('@/components/UI/Images/' + image)"
          width="80"
          height="80"
        />

        <div class="swiper" :class="swiperUniqueId">
          <div class="swiper-wrapper">
            <div class="swiper-slide" v-for="quote in quotes" :key="quote">
              <span class="quoteSpan">{{ quote }}</span>
            </div>
          </div>
          <div class="swipper-dots">
            <div class="swiper-pagination"></div>
          </div>
        </div>
      </div>
    </base-card>
  </li>
</template>

<script>
import Swiper, { Pagination, Navigation } from "swiper";
import "/node_modules/swiper/swiper.css";
import "/node_modules/swiper/modules/navigation/navigation.min.css";
import "/node_modules/swiper/modules/pagination/pagination.min.css";

export default {
  props: ["title", "quotes", "image"],
  data() {
    return {
      currentIndex: 0,
      swiperUniqueId: 0,
    };
  },
  created() {
    this.swiperUniqueId = "swiper_" + (Math.random() * 100000).toFixed(0);
  },
  mounted() {
    new Swiper(`.${this.swiperUniqueId}`, {
      modules: [Pagination, Navigation],
      on: {
        slideChange: function (param) {
          console.log("swiper initialized");
          console.log(param.activeIndex);
        },
      },
      pagination: {
        el: ".swiper-pagination",
      },

      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
    });
  },
  methods: {
    goToNextQuote() {
      const lastIndex = this.quotes.length - 1;

      if (this.currentIndex === lastIndex) {
        this.currentIndex = 0;
        return;
      }

      this.currentIndex++;
    },

    goToPreviousQuote() {
      if (this.currentIndex === 0) {
        return;
      }

      this.currentIndex--;
    },
  },
};
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
  align-content: center;
}

.card-body {
  display: grid;
  grid-template-columns: 1fr 4fr;
  align-items: center;
  padding: 5px;
}

.base-card {
  display: grid;
  grid-template-rows: 40px 1fr;
}

.quoteSpan {
  padding: 8px;
  font-style: italic;
  height: calc(100% - 30px);
}

.noborder {
  border: none;
  padding: 0;
  background: none;
}

.nagivation-btns {
  display: flex;
  gap: 4px;
}

.swiper {
  width: 100%;
}

.swiper-pagination {
  bottom: -3px;
}

.swipper-dots {
  padding: 11px;
}

.swiper-wrapper {
  padding-left: 10px
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
  align-content: center;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>