<template>
  <div>
    <h1>Find something to do.</h1>

    <div class="activity-buttons">
      <span
        class="activity-btn"
        @click="getActivity('education')">
          [ Education ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('recreational')">
          [ Recreational ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('social')">
          [ Social ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('diy')">
          [ DIY ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('charity')">
          [ Charity ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('cooking')">
          [ Cooking ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('relaxation')">
          [ Relaxation ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('music')">
          [ Music ]
      </span>
      <span
        class="activity-btn"
        @click="getActivity('busywork')">
          [ Busywork ]
      </span>
    </div>

    <div class="content">
      <h3>{{ activity.text }}</h3>
      <h5><a :href="activity.url">{{ activity.url }}</a></h5>

      <h6 v-if="loading">Fetching activity...</h6>
    </div>
  </div>

</template>

<script>
import axios from 'axios';

export default {
  data(){
    return {
      loading: false,
      activity: {
        text: "",
        url: ""
      }
    }
  },
  methods: {
    getActivity(type){
      this.loading = true
      axios.get("https://www.boredapi.com/api/activity", {
        params: {
          type: type
        }
      }).then(response => {
        this.activity.text = response.data.activity
        this.activity.url = response.data.link
        this.loading = false
      })
    }
  }
}
</script>

<style>
.activity-buttons {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.activity-btn {
  cursor: pointer;
  margin: 10px;
}

.activity-btn:hover {
  color: crimson;
  transition: 0.1s;
}

.content {
  padding-top: 20px;
}

</style>
