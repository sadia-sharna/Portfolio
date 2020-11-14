<style>

.darkblack-bg {
    background: black;
    /* background: #24292e; */
}

.darkyellow-bg {
    background: #f4c818;
}

</style>

<template>
<div>
    <div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{mostUsedTechTitle}}

    </div>
    <div class="card-body text-left font-14">
        <p>
          <div class="row">

                <canvas id="pieChartofCode" class="col-sm-6"></canvas>


                <canvas id="pieChartofDB" class="col-sm-6"></canvas>


          </div>
          <div class="row">
                <canvas id="pieChartofFramework" class="col-sm-6 mx-auto"></canvas>

          </div>


        </p>
      </div>
</div>
<div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{title}}

    </div>
    <div class="card-body text-left font-14">
        <p>
            <div class="btn-group flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Code</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.code">{{item}}</button>
            </div>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Framework</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.framework">{{item}}</button>
            </div>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Runtime Environment</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.runtimeEnvironment">{{item}}</button>
            </div>

            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Database</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.database">{{item}}</button>
            </div>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">ORM</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.orm">{{item}}</button>
            </div>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Version Control</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.versionControl">{{item}}</button>
            </div>
            <br>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">Cloud</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.cloud">{{item}}</button>
            </div>
            <br>
            <div class="btn-group mt-2 flex-wrap" role="group" aria-label="Basic example">
                <button type="button" class="btn darkblack-bg text-white">OS</button>
                <button type="button" class="btn darkyellow-bg" v-for="item in skillSet.os">{{item}}</button>
            </div>


        </p>

    </div>
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
        mostUsedTechTitle: String,

    },
    data() {
        return {
            skillSet: {
                code: [],
                framework: [],
                database: [],
                versionControl: [],
                cloud: [],
                os: [],
                orm: [],
                runtimeEnvironment:[],

            },
            mostUsedTechList: [],
        }
    },
    mounted() {
      this.getSkillSet();
      this.getMostUsedTechPercntgWithLabel();



    },

    methods: {
      getMostUsedTechPercntgWithLabel(){
        this.mostUsedTechList = {
          pieChartofCode : {
            labels: ["C#", "JavaScript", "Python", "C++", "Java", "C"],
            data:[35, 40, 10, 15, 7, 3],
          },
          pieChartofFramework : {
            labels: ["Vue.js", "ASP.NET Core", "ASP.NET MVC", "AngularJS"],
            data:[30, 20, 15, 15],
          },
          pieChartofDB : {
            labels: ["SQL", "SQLite","MongoDB", "MySQL", "PL/SQL"],
            data:[50, 25, 5, 15, 5],
          },

        };
        for (var key in this.mostUsedTechList) {
          //console.log(key + " -> " + p[key]);
          this.getPieChart(this.mostUsedTechList[key], key);

        }
        // this.getPieChart(this.mostUsedTechList.pieChartofCode);


      },
      getSkillSet(){
      this.skillSet.code.push("C#", "JavaScript", "Python", "C++", "Java", "C");
      this.skillSet.framework.push("ASP.NET Core", "ASP.NET MVC", "Vue.js", "AngularJS", "LINQ");
      this.skillSet.database.push("SQL", "SQLite","MongoDB", "MySQL", "PL/SQL");
      this.skillSet.orm.push("Entity Framework", "Entity Framework Core");
      this.skillSet.runtimeEnvironment.push("Node.js");
      this.skillSet.versionControl.push("Git", "TFS");
      this.skillSet.cloud.push("Azure");
      this.skillSet.os.push("Windows", "Linux");

      },
      getPieChart(item, chartId) {
              let colorsList = [];
              let i;

              for (i = 0; i < item.labels.length; i++) {
                  colorsList.push('#' + ((Math.random() * 0xffffff) << 0).toString(16));
              }

              var ctx = document.getElementById(chartId).getContext('2d');
              // if (this.chartId) {
              //     this.chartId.destroy();
              // }
              this.chartId = new Chart(ctx, {
                  type: 'pie',
                  data: {
                      labels: item.labels,
                      datasets: [{
                          backgroundColor: colorsList,
                          data: item.data
                      }],

                  },

              });
          },


    },
}

</script>
