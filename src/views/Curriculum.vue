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
        <ul class="list-group list-group-flush" v-for="item in curriculumList">

            <a  class="list-group-item list-group-item-action bg-light">
                <div class="list-group-item-heading font-weight-bold">{{item.curriculumTitle}} </div>

            </a>

            <li class="list-group-item">
                {{item.curriculumDescription}}
            </li>






        </ul>

    </div>
</div>

</template>

<script>

// @ is an alias to /src
//import TitleWithDescriptionCard from '@/components/TitleWithDescriptionCard.vue';
// import About from '@/views/About.vue';

export default {
    name: 'Curriculum',
    props: {
        title: String,


    },

    data() {
        return {
            curriculumList: [],

        }
    },
    mounted() {
        this.getCurriculumData();

    },
    methods: {
        getCurriculumData() {

            this.curriculumList.push({
                    curriculumTitle: "Organizing Codeware",
                    curriculumDescription: "Organized Intra AUST Project Show, Intra AUST Programming Contest and Intra AUST Quiz Contest.",
                }

            );
        },
    },
}

</script>
