<style>

.font-14 {
    font-size: 14px;
}

.darkblue-bg {
    /* background: #21223e; */
    background: #303156;
}

</style>

<template>

<div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{title}}

    </div>
    <div class="card-body text-left font-14">
        <ul class="list-group list-group-flush" v-for="item in contestDataList">

                <a href="#" class="list-group-item list-group-item-action bg-light">
                    <div class="list-group-item-heading font-weight-bold">{{item.contestPlatform}} (Id: {{item.contestId}})</div>

                </a>

                <li class="list-group-item">
                    {{item.contestDescription}}
                </li>






        </ul>

    </div>
</div>

</template>

<script>

// @ is an alias to /src
import TitleWithDescriptionCard from '@/components/TitleWithDescriptionCard.vue';
// import About from '@/views/About.vue';

export default {
    name: 'Skills',
    props: {
        title: String,


    },
    components: {
        TitleWithDescriptionCard
    },
    data() {
        return {
          contestDataList: [],

        }
    },
    mounted(){
      this.getContestData();

    },
    methods:{
      getContestData(){

        this.contestDataList.push(
          {
            contestId: '75603',
            contestPlatform : "UVA Online Judge",
            contestDescription : "Solved 84 problems"

          },
          {
            contestId: "Sadia_Sharna",
            contestPlatform : "Codeforces",
            contestDescription : "Contest rating: 896. Participated in 21 contests"
          },
          {
            contestId: "s_sharna06",
            contestPlatform : "HackerRank",
            contestDescription : "2 star in problem solving, 3 star in Python, 2 star in Javascript"

          },
          {
            contestId: "59336",
            contestPlatform : "URI Online Judge",
            contestDescription : "Solved 107 problems"

          },
        );
      },
    },
}

</script>
