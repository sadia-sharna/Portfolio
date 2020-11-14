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
<div>
    <div class="container">
        <div id="top" class="card bg-light ">
            <div class="card-body text-center">
                <!--
            <div class=" mb-3">
                <h2 class="card-text">Welcome to my portfolio! <i class="fa fa-smile-o" style="font-size:48px;color:#56619a"></i></h2>
            </div> -->

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
                                    <div class="card-header text-left darkblue-bg text-white">
                                        Contact Information

                                    </div>
                                    <div class="card-body text-left font-14">
                                        <ul class="list-group list-group-flush">
                                            <!-- <li class="list-group-item"> <i class="fa fa-phone" aria-hidden="true"></i> +8801914658423</li> -->
                                            <li class="list-group-item"> <i class="fa fa-envelope" aria-hidden="true"></i> s.sharna06@gmail.com</li>
                                            <a href="https://github.com/sadia-sharna" target="_blank" class="list-group-item list-group-item-action"><i class="fa fa-github" aria-hidden="true"></i> sadia-sharna</a>
                                            <a href="https://www.linkedin.com/in/sadia-tasnim-b82aa7160/?originalSubdomain=bd" target="_blank" class="list-group-item list-group-item-action"><i class="fa fa-linkedin-square" aria-hidden="true"></i> sadia-tasnim-b82aa7160ac</a>
                                            <a href="https://codepen.io/sadia-sharna" target="_blank" class="list-group-item list-group-item-action"><i class="fa fa-codepen" aria-hidden="true"></i> codepen.io/sadia-sharna</a>

                                        </ul>

                                    </div>
                                </div>
                                <ProblemSolving title="Problem Solving" />
                                <Achievements title="Achievements" />
                                <Curriculum title="Curriculum Activities" />
                                <Reference title="Reference" />

                            </div>

                        </div>
                    </div>
                    <div class="col-sm-8">
                        <div class="card">

                            <div class="card-body text-left">

                                <!-- <TitleWithDescriptionCard title = "Professional Summary"
                          description = "Results-oriented software engineering professional with
                          expertise in building scalable applications. Excellent team player
                          with a positive attitude. Quickly learn and master new
                          technologies and working in both team and self-directed
                          settings. Very Passionate and honest."/> -->

                                <Aboutme title="Who am I?" />
                                <Skills title="Tools & technologies" mostUsedTechTitle="Most Used Technologies" />
                                <Projects title="Pet Projects" />

                            </div>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </div>
    <!-- <a href="#top" class="float-right mr-5"> <i class=" border p-2 mb-3 fa fa-arrow-up"></i></a> -->

</div>
</template>

<script>
// @ is an alias to /src
import Aboutme from '@/views/Aboutme.vue';
import Skills from '@/views/Skills.vue';
import ProblemSolving from '@/views/ProblemSolving.vue';
import Projects from '@/views/Projects.vue';
import Reference from '@/views/Reference.vue';
import Achievements from '@/views/Achievements.vue';
import Curriculum from '@/views/Curriculum.vue';

export default {
    name: 'Home',
    components: {
        Aboutme,
        Skills,
        ProblemSolving,
        Projects,
        Reference,
        Achievements,
        Curriculum
    },
    data() {
        return {
            jobStartmonth: 6,
            jobStartyear: 2019,
            jobDuration: '',
        }
    },

}
</script>
