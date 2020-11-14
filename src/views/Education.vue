<template>
<div class="card border-0">
    <div class="card-header text-left darkblue-bg text-white">
        {{title}}

    </div>
    <div class="card-body text-left font-14">
        
       
            <div class=" px-3 ">
                <div class="row font-weight-bold card-title text-info  " style="font-size:16px;">Bachelor of Science Computer Science And Engineering</div>
                <div class="row card-text text-success">Ahsanullah University Of Science & Technology </div>
                <div class="row mt-1 mb-1 text-secondary"> Apr 2014 - Jun 2019</div> 
                <div class="row card-text ">Graduated with - 3.55 out of 4.00 CGPA </div>
               
                <div class="row font-weight-bold card-title text-info  mt-4" style="font-size:16px;">Higher Secondary Certificate</div>
                <div class="row card-text text-success">Viqarunnisa Noon School & College </div>
                <div class="row mt-1 mb-1 text-secondary"> Apr 2012 - May 2014</div> 
                <div class="row card-text ">Graduated with 5.00 out of 5.00 GPA</div>
               
               
                
            </div>
           
           

       

    </div>
</div>
</template>

<script>
export default {
    name: 'Education',
    props: {
        title: String,

    },
   
   

}
</script>
