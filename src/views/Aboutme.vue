<template>
  <div class="card border-0">
      <div class="card-header text-left darkblue-bg text-white">
        {{title}}

      </div>
      <div class="card-body text-left font-14">
        <p>
            {{aboutmeDescription}}
        </p>

      </div>
  </div>

</template>

<script>
export default {
  name: 'Aboutme',
  props: {
    title : String,
    
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
