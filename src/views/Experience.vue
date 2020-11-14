<template>
<div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{title}}

    </div>
    <div class="card-body text-left font-14">
        <div>
            <div class="card px-5 py-4 shadow">
                <div class="row font-weight-bold card-title text-info  " style="font-size:16px;">Associate Software Engineer</div>
                <div class="row card-text text-success">Syntec Consulting Limited </div>
                <div class="row mt-1 mb-1 text-secondary"> Oct 2019 - Present</div>
                <div class="ml-4">
                    <div class="row font-italic ">Responsibilities:</div>
                    <div class="row">
                        <ul>
                            <li>Developing new modules and modifying existing modules</li>
                            <li>Colaborating with UI/UX and Senior developers</li>
                      
                        </ul>

                    </div>
                </div>
                <div class="ml-4">
                    <div class="row font-italic">
                        Technologies:

                    </div>
                    <div class="row">
                        <ul>

                            <li>
                                Front-end: Vue.js and AngularJS
                            </li>
                            <li>
                                Back-end: C#, ASP.NET Web API, ASP.NET Core Web API, Entity Framework in db-first
                                approach
                            </li>
                            <li>Database: Microsoft SQL Server, SQLite</li>
                        </ul>
                    </div>
                </div>
            </div>
             <div class="card px-5 py-4 shadow mt-5">
                <div class="row font-weight-bold card-title text-info  " style="font-size:16px;">Software Engineering Intern</div>
                <div class="row card-text text-success">Syntec Consulting Limited </div>
                <div class="row mt-1 mb-1 text-secondary"> Jul 2019 - Sep 2019</div>
                <div class="ml-4">
                    <div class="row font-italic ">Responsibilities:</div>
                    <div class="row">
                        <ul>
                            <li>Creating project as assignment to get adapted with the technologies</li>
                            <li>Working in the main project</li>
                         
                      
                        </ul>

                    </div>
                </div>
                <div class="ml-4">
                    <div class="row font-italic">
                        Technologies:

                    </div>
                    <div class="row">
                        <ul>

                            <li>
                                Front-end: AngularJS
                            </li>
                            <li>
                                Back-end: C#, ASP.NET Web API, Entity Framework in db-first approach
                            </li>
                            <li>Database: Microsoft SQL Server</li>
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
    name: 'Experience',
    props: {
        title: String,

    },
   
   

}
</script>
