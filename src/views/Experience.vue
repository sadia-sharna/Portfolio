<template>
  <div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
      {{ title }}
    </div>
    <div class="card-body text-left font-14">
      <div>
        <div
          class="card px-5 py-4 mb-1 shadow"
          v-for="(item, index) in experienceList"
        >
          <div
            class="row font-weight-bold card-title text-info "
            style="font-size:16px;"
          >
            {{ item.designation }}
          </div>
          <div class="row card-text text-success">
            {{ item.companyName }}
          </div>
          <div class="row mt-1 mb-1 text-secondary">{{ item.duration }}</div>
          <div class="ml-4">
            <div class="row font-italic ">Responsibilities:</div>
            <div class="row">
              <ul>
                <li v-for="(res, ind) in item.responsibilities">{{ res }}</li>
              </ul>
            </div>
          </div>
          <div class="ml-4">
            <div class="row font-italic">
              Technologies:
            </div>
            <div class="row">
              <ul>
                <li v-for="(techValue, techName) in item.technologies">
                  {{ techName }}: {{ techValue }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",
  props: {
    title: String,
  },
  data() {
    return {
      experienceList: [
        {
          designation: "Associate Software Engineer",
          companyName: "Kaz Software",
          duration: "Feb 2021 - Present",
          responsibilities: [
            "Became an integral part of the team ",
            "Worked in both frontend and backend on different technologies",
            "Guided junior developers/interns to work on team projects and helped them perform different tasks",
          ],
          technologies: {
            "Front-end": "React.js and Angular 10",
            "Back-end":
              "C#, ASP.NET Web API, ASP.NET Core Web API, Entity Framework in db-first approach",
            Database: "Microsoft SQL Server, MySql",
          },
        },
        {
          designation: "Associate Software Engineer",
          companyName: "Syntec Consulting Limited",
          duration: "Oct 2019 - Jan2021",
          responsibilities: [
            "Developing new modules and modifying existing modules",
            "Colaborating with UI/UX and Senior developers",
          ],
          technologies: {
            "Front-end": "Vue.js and AngularJS",
            "Back-end":
              "C#, ASP.NET Web API, ASP.NET Core Web API, Entity Framework in db-first approach",
            Database: "Microsoft SQL Server, SQLite",
          },
        },
        {
          designation: "Software Engineering Intern",
          companyName: "Syntec Consulting Limited",
          duration: "Jul 2019 - Sep 2019",
          responsibilities: [
            "Creating project as assignment to get adapted with the technologies",
            "Working in the main project",
          ],
          technologies: {
            "Front-end": "AngularJS",
            "Back-end":
              "C#, ASP.NET Web API, Entity Framework in db-first approach",
            Database: "Microsoft SQL Server",
          },
        },
      ],
    };
  },
};
</script>
