<template>
    <div> 
        <div class="col-md-12">
            
        
        <div class="card">
            <img class="card-img-top" src="holder.js/100x180/" alt="">
            <div class="card-body">
                <h4 class="card-title">Title</h4>
                <p class="card-text">Text</p>
            </div>
        </div>
        {{maison.id}}
        {{maison.prix}}
        </div>
    </div>
</template>


<script>
export default {
    name : 'Maison',
    props  : ['maison']
}
</script>

