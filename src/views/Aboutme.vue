<template>
  <div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
      {{ title }}
    </div>
    <div class="card-body text-left font-14">
      <p>
        {{ aboutmeDescription }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Aboutme",
  props: {
    title: String,
  },
  data() {
    return {
      jobStartmonth: 6,
      jobStartyear: 2019,
      jobDuration: "",
      aboutmeDescription: `I'm a Software Engineer from Bangladesh. I'm a true fan of competitive programming and web development. I love learning new technologies and playing with them`,
    };
  },
};
</script>
