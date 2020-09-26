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

            },
        }
    },
    mounted() {
      this.getSkillSet();


    },

    methods: {
      getSkillSet(){
      this.skillSet.code.push("C#", "JavaScript", "Python", "C++", "Java", "C");
      this.skillSet.framework.push("ASP.NET Core", "ASP.NET MVC", "Vue.js", "AngularJS", "LINQ");
      this.skillSet.database.push("SQL", "SQLite","MongoDB", "MySQL", "PL/SQL");
      this.skillSet.orm.push("Entity Framework", "Entity Framework Core");
      this.skillSet.versionControl.push("Git", "TFS");
      this.skillSet.cloud.push("Azure");
      this.skillSet.os.push("Windows", "Linux");

      },

    },
}

</script>
