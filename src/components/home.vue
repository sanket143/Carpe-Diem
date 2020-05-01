<template>
  <div>
    <h1>Find something to do.</h1>

    <div class="activity-buttons">
      <span class="activity-btn">[ Education ]</span>
      <span class="activity-btn">[ Recreational ]</span>
      <span class="activity-btn">[ Social ]</span>
      <span class="activity-btn">[ DIY ]</span>
      <span class="activity-btn">[ Charity ]</span>
      <span class="activity-btn">[ Cooking ]</span>
      <span class="activity-btn">[ Relaxation ]</span>
      <span class="activity-btn">[ Music ]</span>
      <span class="activity-btn">[ Busywork ]</span>
    </div>
  </div>

</template>

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
  transition: 0.2s;
}

</style>
