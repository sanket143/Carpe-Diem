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
  </div>

</template>

<script>
export default {
  methods: {
    getActivity(type){
      console.log(type);
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

</style>
