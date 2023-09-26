<template>
    

        <div class="container">

                <div v-if="showaddform" class="pop-up">
                
                    <addToDoForm/>
                </div>
                   
                    
                
                <div class="content">
                    <div style="padding: 20px">
                        <h1 style="margin-left: 20px;;">Today</h1>
                        <p style="color:grey;margin-left: 20px;">18th June 2019,Tuesday</p>
                    </div>
                

                    <div v-for= "item in tasks" class="task">
                    <div>
                        <h2 style="margin-left:20px;">{{ item.title }}</h2>
                        <p style="color:grey;margin-left:20px;">{{ item.description }}</p>
                    </div>
                    <div >

                        <p style="color:grey">9:30 A.M.</p>
                        <img src="../assets/profile pic.jpg" class="image">
                    </div>
                    
                     </div>

                     
           
                 </div>
                 <div style="padding: 30px;" >
                    <button @click="addtodoform" class="btn"> + Add new task</button>
                 </div>
          
        </div>

   
  
</template>

<script>
import addToDoForm from '../components/addToDoForm.vue';
export default{
  components: { addToDoForm },
    data(){
        return{
            tasks:[
                {title:"Project daily stand-up",description:"At the conference centre"},
            {title:"Internia new UI style",description:"Remember to bring presents"},
            {title:"Weekly review",description:"Wanda square E5"},
            {title:"Interview ",description:"Remember to bring laptop "},

           
        
        ],
        showaddform: false
        }
   


    },
    methods :{

    addtodoform()
    {
       
        this.showaddform=!this.showaddform
    }

    }
   
}


</script>

<style scoped>
.container{
    background:rgb(222, 193, 140);
    border:1px solid rgb(222, 193, 140);
    position:relative;
    
    
    
}

.content{
    background:white;
    border-radius:50px;
    margin:40px;
   
   
   
}

.task{
    background: white;
    border-radius: 20px;
    border: none;
    margin-top: 15px;
    margin-left: 20px;
    margin-right: 20px;
    box-shadow: 5px 10px 18px #888888;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.btn{
    padding: 35px;
    width: 100%;
    border-radius: 50px;
    border: none;
    background: cornflowerblue;
    color: white;
    font-size: 25px;
}

.image{
    height: 25px;
    width: 25px;
    border-radius: 25px;
    margin-right: 20px;
}

.pop-up{
    
    background:pink;
    position:absolute;
    left: 40%;
    bottom: 35%;
    height: 400px;
    width: 400px;

    
    

}
</style>


