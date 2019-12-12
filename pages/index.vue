<style>
* {
  box-sizing: border-box;
}
.clear {
  clear: both;
}
h3 {
  color: black;
}
h5 {
  color: rgb(148, 148, 148);
  display: inline;
  margin: 10px 0px 10px 0px;
}
#container {
  width: 65%;
  height: auto;
  margin: auto;
  padding-top: 70px;
  display: flex;
  flex-wrap: wrap;
}
#box {
  width: 47%;
  height: auto;
  margin: 10px;
  padding: 15px;
  background-color: white;
}
#faIcon {
  margin-right: 20px;
}
</style>
<template>
  <v-container id="container">
    <div id="box">
      <h3>spa</h3>
      <h5>
        <span>
          <font-awesome-icon :icon="['fas', 'mobile']" />
        </span>
        840 users
      </h5>
      <h5>
        <span>
          <font-awesome-icon :icon="['fab', 'chrome']" />
          <font-awesome-icon :icon="['fab', 'apple']" />
        </span>
      </h5>
      <h5 style="float:right;">
        <button>
          <font-awesome-icon :icon="['fas', 'ellipsis-v']" />
        </button>
      </h5>
      <div class="clear"></div>
      <line-chart></line-chart>
      <h5>
        <span>
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'paper-plane']"
            size="lg"
          />
          <font-awesome-icon id="faIcon" :icon="['fas', 'clock']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'mobile']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'users']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'cog']" size="lg" />
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'chart-area']"
            size="lg"
          />
        </span>
      </h5>
    </div>
    <div id="box">
      <h3>EldolarLive</h3>
      <h5>
        <span>
          <font-awesome-icon :icon="['fas', 'mobile']" />
        </span>
        840 users
      </h5>
      <h5>
        <span>
          <font-awesome-icon :icon="['fab', 'chrome']" />
          <font-awesome-icon :icon="['fab', 'apple']" />
        </span>
      </h5>
      <h5 style="float:right;">
        <button>
          <font-awesome-icon :icon="['fas', 'ellipsis-v']" />
        </button>
      </h5>
      <div class="clear"></div>
      <line-chart></line-chart>
      <h5>
        <span>
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'paper-plane']"
            size="lg"
          />
          <font-awesome-icon id="faIcon" :icon="['fas', 'clock']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'mobile']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'users']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'cog']" size="lg" />
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'chart-area']"
            size="lg"
          />
        </span>
      </h5>
    </div>
    <div id="box">
      <h3>PushBots</h3>
      <h5>
        <span>
          <font-awesome-icon :icon="['fas', 'mobile']" />
        </span>
        840 users
      </h5>
      <h5>
        <span>
          <font-awesome-icon :icon="['fab', 'chrome']" />
          <font-awesome-icon :icon="['fab', 'apple']" />
        </span>
      </h5>
      <h5 style="float:right;">
        <button>
          <font-awesome-icon :icon="['fas', 'ellipsis-v']" />
        </button>
      </h5>
      <div class="clear"></div>
      <line-chart></line-chart>
      <h5>
        <span>
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'paper-plane']"
            size="lg"
          />
          <font-awesome-icon id="faIcon" :icon="['fas', 'clock']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'mobile']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'users']" size="lg" />
          <font-awesome-icon id="faIcon" :icon="['fas', 'cog']" size="lg" />
          <font-awesome-icon
            id="faIcon"
            :icon="['fas', 'chart-area']"
            size="lg"
          />
        </span>
      </h5>
    </div>
  </v-container>
</template>

<script>
import axios from 'axios'
import LineChart from '@/components/LineChart'
export default {
  components: { LineChart },

  /*  async asyncData() {
    const { data } = await axios.get(`
    https://newsapi.org/v2/top-headlines?country=us&category=music&apiKey=6ae3e6f1aed346f993acd380ae98acaf`)
    return { title: data.articles[0].title }
  } */
  async asyncData() {
    const { data } = await axios.get(`
    https://newsapi.org/v2/top-headlines?country=us&category=music&apiKey=6ae3e6f1aed346f993acd380ae98acaf`)
    return { articles: data.articles }
  }

  /*  asyncData() {
    return axios
      .get(
        `https://newsapi.org/v2/top-headlines?country=us&category=music&apiKey=6ae3e6f1aed346f993acd380ae98acaf`
      )
      .then((res) => {
        return { titles: res.articles[0].title }
      })
  } */
}
</script>
