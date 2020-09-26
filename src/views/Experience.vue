<style>

.font-14 {
  font-size:14px;
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
                                        <a href="https://github.com/sadia-sharna" class="list-group-item list-group-item-action"><i class="fa fa-github" aria-hidden="true"></i> sadia-sharna</a>
                                        <a href="https://www.linkedin.com/in/sadia-tasnim-b82aa7160/?originalSubdomain=bd" class="list-group-item list-group-item-action"><i class="fa fa-linkedin-square" aria-hidden="true"></i> sadia-tasnim-b82aa7160ac</a>
                                    </ul>

                                </div>
                            </div>



                        </div>

                    </div>
                </div>
                <div class="col-sm-8">
                    <div class="card">

                      <div class="card-body text-left">

                          <TitleWithDescriptionCard title = "Who am I?"
                          description = "  I'm a software engineer from Bangladesh. I'm a true fan of in competitive programming and web development.
                             Currently, I am working at Syntec Consulting Limited which provides solution for Healthcare (EHR and EMR)."/>

                          <!-- <TitleWithDescriptionCard title = "Professional Summary"
                          description = "Results-oriented software engineering professional with
                          expertise in building scalable applications. Excellent team player
                          with a positive attitude. Quickly learn and master new
                          technologies and working in both team and self-directed
                          settings. Very Passionate and honest."/> -->







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
// import About from '@/views/About.vue';

export default {
    name: 'Experience',
    components: {
      TitleWithDescriptionCard
    },
    data() {
        return {
            userdata: {
                name: 'Sadia',
                sex: 'Female',
                age: 23
            },

        }
    },
}

</script>
