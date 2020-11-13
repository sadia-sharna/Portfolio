<style>

.darkblack-bg {
    background: black;
    /* background: #24292e; */
}

.darkyellow-bg {
    background: #f4c818;
}

.min-height-90{
  min-height: 90%;
}

</style>

<template>
<div>
<div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{title}}

    </div>
    <div class="card-body text-left font-14">
        <p>
          <div class="row">
            <div class="col-sm-6 mb-1" v-for="(item, ind) in petProjectList" :key="ind">
              <div class="card shadow p-3 mb-5 bg-white rounded min-height-90" >
                <img  v-if="item.projectImage" v-bind:src="getImgUrl(item.projectImage)" alt="Project" class="img-thumbnail rounded w-100 " style="height:20%;">

                <div class="card-body">
                  <a :href="item.projectLink" target="_blank" class="btn btn-primary float-right"><i class="fa fa-link"></i></a>

                  <h5 class="card-title text-info">{{item.projectTitle}}</h5>
                    <p class="card-text text-success">{{item.projectTools}}</p>
                  <p class="card-text">{{item.projectDescription}}</p>
                </div>
              </div>

            </div>

          </div>


        </p>

    </div>
</div>

</div>

</template>

<script>


export default {
    name: 'Projects',
    props: {
        title: String,


    },

    data() {
        return {
          petProjectList: [],

        }
    },
    mounted(){
      this.getPetProjectData();

    },
    methods:{
      getImgUrl(itemImg) {
        if(itemImg)
        {
         var images = require.context('../assets/', false,);
         return images('./' + itemImg);
        }
       },
      getPetProjectData(){

        this.petProjectList.push(
          {
            projectTitle: 'Portfolio',
            projectTools : "Vue.js, Bootstrap 4",
            projectDescription : "In this project I have created my personal portfolio where all my skills and projects are highlighted and various charts has been used to show my expertise in all the fields I have interest or familiar with.",
            projectLink:"https://github.com/sadia-sharna/Portfolio",
            projectImage:"Portfolio.jpg",
          },
          {
            projectTitle: 'CarStoreUI',
            projectTools : "Vue.js",
            projectDescription : "This is a single page application with features like CRUD, Autocomplete Search. Cars can be viewed via pie charts Manufacturer Wise and in pagination with details.",
            projectLink:"https://github.com/sadia-sharna/CarStoreUI",
            projectImage:"CarStore.jpg",
          },
          {
            projectTitle: 'CarStoreAPI',
            projectTools : "ASP. NET Web API 2.0, DB:SQL, Cloud: Azure",
            projectDescription : "API for Autocomplete Search, Pagination and CRUD support is written for CarStoreUI Application.",
            projectLink:"https://github.com/sadia-sharna/CarStore",
            projectImage:"CarStore.jpg",
          },
          {
            projectTitle: 'Todolist',
            projectTools : "Vue.js, Vuex",
            projectDescription : "This is a single page application for tracking daily todolists.",
            projectLink:"https://awesome-lichterman-e2dc1b.netlify.app/#/",
            projectImage:"Todolist.jpg",
          },
          {
            projectTitle: 'ResumeMakerUI',
            projectTools : "AngularJS",
            projectDescription : "A single page application where user can give all the Basic Information(Introduction, Skills, Education, Curricular Activities and Reference) as input and it will create a nice resume for him/her.",
            projectLink:"https://github.com/sadia-sharna/ResumeMakerApplication",
            projectImage:"ResumeMaker.jpg",
          },
          {
            projectTitle: 'ResumeMakerAPI',
            projectTools : "ASP.NET Web API, C#. DB: SQL",
            projectDescription : "API for storing and fetching user intput data to help the ResumeMakerUI application create a resume for the user.",
            projectLink:"https://github.com/sadia-sharna/ResumeMakerApplication",
            projectImage:"ResumeMaker.jpg",
          },

        );
      },
    },
}

</script>
