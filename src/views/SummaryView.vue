<style>
.font-14 {
    font-size: 14px;
}
.active{
  color: white !important;
  background-color: #303156!important;
}
/* .nav-item > a:hover {
  color: aqua;
} */
</style>

<template>
<div class="container">
    <div class="card bg-light">
        <div class="card-body text-center">

            <div class="row">
                <div class="col-sm-4">
                    <div class="card ">
                        <div class="card-body ">

                            <img alt="Sadia Tasnim" src="../assets/Sadia.jpg" class="rounded-circle  w-50 ">
                            <h3>Sadia Tasnim</h3>
                            <div class="text-center">
                                Associate Software Engineer
                               
                            </div>
                            <div>
                                 <a class="mr-1" href = "mailto: s.sharna06@gmail.com"> <i class="fa fa-envelope" aria-hidden="true"></i> </a>|
                                        <a class="mr-1" href="https://github.com/sadia-sharna" target="_blank" ><i class="fa fa-github" aria-hidden="true"></i></a>|
                                        <a class="mr-1" href="https://www.linkedin.com/in/sadia-tasnim-b82aa7160/?originalSubdomain=bd" target="_blank"><i class="fa fa-linkedin-square" aria-hidden="true"></i></a>|
                                        <a class="mr-1" href="https://codepen.io/sadia-sharna" target="_blank" ><i class="fa fa-codepen" aria-hidden="true"></i> </a>

                            </div>
                            <hr class="border">

                            <div class="card border-0">
                                <!-- <div class="card-header text-left darkblue-bg text-white">
                                    Contact Information

                                </div> -->
                                <div class="card-body text-left font-14">

                                    <div class="nav flex-column nav-pills" id="v-pills-tab" role="tablist" aria-orientation="vertical" style="cursor:pointer;">
                                        <a class="nav-link active" data-toggle="pill" role="tab"  @click="showItem='aboutme'">About Me</a>
                                        <a class="nav-link" data-toggle="pill" role="tab" @click="showItem='experience'">Experience</a>
                                        <a class="nav-link " data-toggle="pill" role="tab"  @click="showItem='project'">Pet Projects</a>
                                        <a class="nav-link" data-toggle="pill" role="tab"  @click="showItem='tool'">Skills</a>

                                    </div>

                                </div>
                            </div>

                        </div>

                    </div>
                </div>
                <div class="col-sm-8">
                    <div class="card">

                        <div class="card-body text-left" style="max-height:31rem; overflow-y:scroll;">
                            <!-- <Aboutme title="Who am I?" /> -->
                            <Aboutme v-show="showItem == 'aboutme'" title="Who am I?" />
                             <Education v-show="showItem == 'aboutme'" title="Education" />
                            <Skills v-show="showItem == 'tool'" title="Tools & technologies" mostUsedTechTitle="Most Used Technologies" />
                            <Projects v-show="showItem == 'project'" title="Pet Projects" />
                            <Experience v-show="showItem == 'experience'" title="Experience "/>

                        </div>
                    </div>
                </div>

            </div>

        </div>
    </div>
</div>
</template>

<script>
// @ is an alias to /src

import Aboutme from '@/views/Aboutme.vue';
import Education from '@/views/Education.vue';
import Skills from '@/views/Skills.vue';
import ProblemSolving from '@/views/ProblemSolving.vue';
import Projects from '@/views/Projects.vue';
import Experience from '@/views/Experience.vue';

export default {
    name: 'SummaryView',
    components: {
        Aboutme,
        Education,
        Skills,
        ProblemSolving,
        Projects,
        Experience
    },
    data() {
        return {
            userdata: {
                name: 'Sadia',
                sex: 'Female',
                age: 23
            },
            showItem: 'aboutme',

        }
    },
}
</script>
