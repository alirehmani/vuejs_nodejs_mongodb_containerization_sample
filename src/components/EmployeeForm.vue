<template>
    <div class="employee">
        <p>{{msg}}</p>
        <button type="button" class="btn btn-primary">Primary</button>
    </div>

</template>


<script>
export  default {

name:'employee',
props:{
    msg:String
}


}

</script>
