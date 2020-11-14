<style>
.font-14 {
    font-size: 14px;
}
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
                            <hr class="border">

                            <div class="card border-0">
                                <!-- <div class="card-header text-left darkblue-bg text-white">
                                    Contact Information

                                </div> -->
                                <div class="card-body text-left font-14">
                                    <!-- <ul class="list-group list-group-flush">
                                      <a class="list-group-item list-group-item-action" @click="showItem='project'"> Projects</a>
                                      <a class="list-group-item list-group-item-action" @click="showItem='tool'"> Skills</a>
                                      <a class="list-group-item list-group-item-action"> Hobbies</a>
                                    </ul> -->
                                    <div class="nav flex-column nav-pills" id="v-pills-tab" role="tablist" aria-orientation="vertical" style="cursor:pointer;">
                                         <a class="nav-link active"  data-toggle="pill"  role="tab"  aria-selected="true" @click="showItem='aboutme'">About Me</a>
                                          <a class="nav-link" data-toggle="pill" role="tab" aria-selected="false" @click="showItem='experience'">Experience</a>
                                        <a class="nav-link " data-toggle="pill"  role="tab"  aria-selected="true" @click="showItem='project'">Projects</a>
                                        <a class="nav-link"  data-toggle="pill" role="tab" aria-selected="false"  @click="showItem='tool'">Skills</a>
                                       
                                    </div>

                                </div>
                            </div>

                        </div>

                    </div>
                </div>
                <div class="col-sm-8">
                    <div class="card">

                        <div class="card-body text-left" style="max-height:475px; overflow-y:scroll;">
                             <!-- <Aboutme title="Who am I?" /> -->
                            <Aboutme v-show="showItem == 'aboutme'" title="About me" />
                            <Skills v-show="showItem == 'tool'" title="Tools & technologies" mostUsedTechTitle="Most Used Technologies" />
                            <Projects v-show="showItem == 'project'" title="Pet Projects" />
                            <Experience v-show="showItem == 'experience'"/>

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
// import About from '@/views/About.vue';
import Skills from '@/views/Skills.vue';
import ProblemSolving from '@/views/ProblemSolving.vue';
import Projects from '@/views/Projects.vue';
import Experience from '@/views/Experience.vue';

export default {
    name: 'SummaryView',
    components: {
        Aboutme,
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
