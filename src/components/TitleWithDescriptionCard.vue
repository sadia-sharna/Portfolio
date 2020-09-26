<template>
  <div class="card border-0">
      <div class="card-header text-left darkblue-bg text-white">
        {{title}}

      </div>
      <div class="card-body text-left font-14">
        <p>
            {{description}}
        </p>

      </div>
  </div>

</template>

<script>
export default {
  name: 'TitleWithDescriptionCard',
  props: {
    title : String,
    description : String,
  }
}
</script>
