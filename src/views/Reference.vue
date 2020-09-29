<template>
  <div class="card border-0">
      <div class="card-header text-left darkblue-bg text-white">
        {{title}}

      </div>
      <div class="card-body text-left font-14">
        <ul class="list-group list-group-flush" v-for="item in referenceList">

                <a  class="list-group-item list-group-item-action bg-light">
                    <div class="list-group-item-heading font-weight-bold">{{item.name}}</div>

                </a>

                <li class="list-group-item">
                  {{item.designation}}
                  <br>{{item.workplace}}
                  <br><span><b>Relation: {{item.relation}}</b></span>
                  <br>
                  <span> <i class="fa fa-phone" aria-hidden="true"></i> {{item.phone}}</span>

                </li>
        </ul>
        <!-- <h6>Mr. Md. Khairul Hasan</h6>
        <p>designation: 'Associate Professor of CSE',</p>
        <p>workplace:'Ahsanullah University of Science & Technology',</p>
        <p>relation: 'Professor'</p> -->
        <!-- <p></p> -->

      </div>
  </div>

</template>

<script>
export default {
  name: 'Reference',
  props: {
    title : String,

  },
  data() {
      return {
        referenceList: [],

      }
  },
  mounted(){
    this.getReferenceData();

  },
  methods:{
    getReferenceData(){
      this.referenceList.push(
        {
          name: 'Mr. Md. Khairul Hasan',
          designation: 'Associate Professor of CSE',
          workplace:'Ahsanullah University of Science & Technology',
          relation: 'Supervisor',
          phone:'+8801711109629'
        },
        {
          name: 'Sakib Eshrak',
          designation: 'Associate Software Engineer',
          workplace:'Syntec Consulting Limited',
          relation: 'Colleague',
          phone:'+8801521207996'
        }
      );

    },
  },
}
</script>
