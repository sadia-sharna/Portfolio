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
        <ul class="list-group list-group-flush" v-for="item in achievementList">

            <a  class="list-group-item list-group-item-action bg-light">
                <div class="list-group-item-heading font-weight-bold">{{item.achivementTitle}} </div>

            </a>

            <li class="list-group-item">
                {{item.achivementDescription}}
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
    name: 'Achievements',
    props: {
        title: String,


    },

    data() {
        return {
            achievementList: [],

        }
    },
    mounted() {
        this.getAchivementData();

    },
    methods: {
        getAchivementData() {

            this.achievementList.push({
                    achivementTitle: "Falguni CodeSprint 2019",
                    achivementDescription: "It was a 2 days Hackathon. Collaborated with team of 5 in the development of Clone of Amazon Search Engine.",
                }, {
                    achivementTitle: 'BUP Hackathon 2019',
                    achivementDescription: "It was 8 hours Hackathon. Collaborated with team of 4 in the development of Vaccine Calendar of a family.",
                }, {
                    achivementTitle: 'Engenius 2018',
                    achivementDescription: '1st Runner-Up in hardware category. Collaborated with team of 4 in the development of CNC Drawing Machine.',
                }, {
                    achivementTitle: 'BITM Web Design course Training',
                    achivementDescription: 'It was a 3 months course. Collaborated with team of 5 in the development of a Clone of Pickaboo Website.',
                }, {
                    achivementTitle: 'Intra AUST Programming Contest',
                    achivementDescription: 'Participated in Intra AUST Programming Contest.',
                }, {
                    achivementTitle: 'Intra AUST Project Show',
                    achivementDescription: 'Participated in Intra AUST Project Show.',
                },


            );
        },
    },
}

</script>
