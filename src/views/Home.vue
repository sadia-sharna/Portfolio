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

<div class="container p-3 my-3 darkblue-bg">
    <div class="card bg-light">
        <div class="card-body text-center">

            <div class=" mb-3">
                <h2 class="card-text">Welcome to my portfolio! <i class="fa fa-smile-o" style="font-size:48px;color:#56619a"></i></h2>
            </div>

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
                                        <li class="list-group-item"> <i class="fa fa-phone" aria-hidden="true"></i> +8801914658423</li>
                                        <li class="list-group-item"> <i class="fa fa-envelope" aria-hidden="true"></i> s.sharna06@gmail.com</li>
                                        <a href="https://github.com/sadia-sharna" target="_blank" class="list-group-item list-group-item-action"><i class="fa fa-github" aria-hidden="true"></i> sadia-sharna</a>
                                        <a href="https://www.linkedin.com/in/sadia-tasnim-b82aa7160/?originalSubdomain=bd" target="_blank" class="list-group-item list-group-item-action"><i class="fa fa-linkedin-square" aria-hidden="true"></i> sadia-tasnim-b82aa7160ac</a>
                                    </ul>

                                </div>
                            </div>
                            <ProblemSolving title="Problem Solving" />




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

                            <TitleWithDescriptionCard title="Who am I?" :description="aboutmeDescription" />
                            <Skills title="Tools & technologies" mostUsedTechTitle="Most Used Technologies" />

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
import TitleWithDescriptionCard from '@/components/TitleWithDescriptionCard.vue';
import Skills from '@/views/Skills.vue';
import ProblemSolving from '@/views/ProblemSolving.vue';

export default {
    name: 'Home',
    components: {
        TitleWithDescriptionCard,
        Skills,
        ProblemSolving
    },
    data() {
        return {
            jobStartmonth: 6,
            jobStartyear: 2019,
            jobDuration: '',
            aboutmeDescription: '',
        }
    },
    mounted() {
        this.jobDuration = this.getExperienceDuration(this.jobStartyear, this.jobStartmonth);
        this.aboutmeDescription = `I'm a software engineer from Bangladesh. I'm a true fan of competitive programming and web development.
         Currently, I am working at Syntec Consulting Limited for ${this.jobDuration.years} yrs and ${this.jobDuration.months} mos which provides solution for Healthcare (EHR and EMR).`;



    },

    methods: {
        getExperienceDuration(year, month) {


            var now = new Date();
            var today = new Date(now.getYear(), now.getMonth(), now.getDate());

            var yearNow = now.getYear();
            var monthNow = now.getMonth();
            var dateNow = now.getDate();

            var dob = new Date(year, month, now.getDate());

            var yearDob = dob.getYear();
            var monthDob = dob.getMonth();
            var dateDob = dob.getDate();
            var age = {};
            var ageString = "";
            var yearString = "";
            var monthString = "";
            var dayString = "";


            var yearAge = yearNow - yearDob;

            if (monthNow >= monthDob)
                var monthAge = monthNow - monthDob;
            else {
                yearAge--;
                var monthAge = 12 + monthNow - monthDob;
            }

            if (dateNow >= dateDob)
                var dateAge = dateNow - dateDob;
            else {
                monthAge--;
                var dateAge = 31 + dateNow - dateDob;

                if (monthAge < 0) {
                    monthAge = 11;
                    yearAge--;
                }
            }

            age = {
                years: yearAge,
                months: monthAge,
                days: dateAge
            };


            return age;



        },
    },
}

</script>
