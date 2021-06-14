

<template>
  <div class="employee">
    <form class="row g-3" v-on:submit.prevent="saveData">
      <div class="col-md-6">
        <label for="firstName" class="form-label">First Name</label>
        <input type="text" class="form-control" v-model="firstName" required/>
      </div>
      <div class="col-md-6">
        <label for="lastName" class="form-label">Last Name</label>
        <input type="text" class="form-control" v-model="lastName" required/>
      </div>
      <div class="col-md-6">
        <label class="form-label">Designation</label>
        <select class="form-select" v-model="desig" required>
          <option selected value="">Choose...</option>
          <option v-for="item in desigArray" :key="item">{{item}}</option>
        </select>
      </div>
      <div class="col-md-6">
        <label class="form-label">Programming Language</label>
        <select class="form-select" v-model="fovProg" required>
          <option selected value="">Choose...</option>
          <option v-for="item in progLang" :key="item">{{item}}</option>
        </select>
      </div>
      <div class="col-12">
        <button type="submit" class="btn btn-secondary">Done</button>
      </div>
    </form>
  </div>
</template>




<script>
import axios from 'axios';
export default {
  name: "employee",
  props: {

    msg: String,
    
  },
  data:function (){
      return{

        desigArray:['UI/UX Engineer','Full Stack Developer','Devops Engineer', "Software Engineer"],
        progLang:["Java","Node","C#","Python","R","Go","Java Script"],
        firstName:'',
        lastName:'',
        desig:'',
        fovProg:''

      }


  },

  methods:{

      saveData:function(){

        console.log(this.firstName+"\n"+this.lastName+"\n"+this.desig+"\n"+this.fovProg);

        axios({
        method:'post',
        url:''
        }).then((res)=>{
        
          console.log(res.data);

        });
      }

  }
};
</script>
