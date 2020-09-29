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
              <!-- <div class="card ">
                <div class="card-body">
                  <h4 class="card-title">Card title</h4>
                  <p class="card-text">Some example text. Some example text.</p>
                  <a href="#" class="card-link">Card link</a>

                </div>
              </div> -->
            </div>

          </div>


        </p>

    </div>
</div>

</div>

</template>

<script>

// @ is an alias to /src
// import TitleWithDescriptionCard from '@/components/TitleWithDescriptionCard.vue';
// import About from '@/views/About.vue';

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
            projectTools : "Node.js, Vue.js, Bootstrap 4",
            projectDescription : "This project is under development.",
            projectLink:"https://github.com/sadia-sharna/Portfolio",
            projectImage:"Portfolio.jpg",

          },
          {
            projectTitle: 'CarStoreUI',
            projectTools : "Vue.js, Node.js",
            projectDescription : "In this project, user can perform CRUD operation, Autocomplete Search, View Cars in Pie chart Manufacturer Wise and a list of Cars with details in pagination.",
            projectLink:"https://github.com/sadia-sharna/CarStoreUI",
            projectImage:"CarStore.jpg",

          },
          {
            projectTitle: 'CarStoreAPI',
            projectTools : "ASP. NET Web API 2.0, DB:SQL, Cloud: Azure",
            projectDescription : "Autocomplete Search, Pagination and CRUD support from API for CarStoreUI Application.",
            projectLink:"https://github.com/sadia-sharna/CarStore",
          //  projectImage:"CarStore.jpg",

          },
          {
            projectTitle: 'ResumeMakerUI',
            projectTools : "AngularJS",
            projectDescription : "This project was a learning project, where User will give all the Basic Information(Introduction, Skills, Education, Curricular Activities and Reference). And It will create a Resume accordingly.",
            projectLink:"https://github.com/sadia-sharna/ResumeMakerApplication",
            projectImage:"ResumeMaker.jpg",

          },
          {
            projectTitle: 'ResumeMakerAPI',
            projectTools : "ASP.NET Web API, C#. DB: SQL",
            projectDescription : "Stores all the user input data and fetch it to show a prepared Resume for ResumeMakerUI application",
            projectLink:"https://github.com/sadia-sharna/ResumeMakerApplication",
            //projectImage:"ResumeMaker.jpg",

          },

        );
      },
    },
}

</script>
