<template>
    

        <div class="container" @click="closepopup">

                <div v-if="showaddform" class="pop-up">
                 <div style="display: flex;justify-content: space-between; align-items: center;">
                    <h1>ToDoItems</h1>
                    <button @click="closepopup" style="background: red; border: none;">X</button>
                 </div>   
                
             <div class="todoform">
             <form style="    font-size: 20px;margin-top: 15%;">
            <label>Title</label><br>
            <input v-model="form.title" type="text" ><br>
            <label>Description</label><br>
            <input v-model="form.description" type="text" ><br><br>
            
             </form>
             <button @click="savetodo" style="padding:10px;">Save</button>
        
             </div>
                  
                </div>
                   
                    
                
                <div class="content">
                    <div style="padding: 15px;display: flex;flex-direction: column;align-items: flex-start;">
                        <h1 >Today</h1>
                        <p style="color:grey;margin:0;">18th June 2019,Tuesday</p>
                    </div>
                

                    <div v-for= "item in tasks" class="task">
                    <div>
                        <h2 style="margin-left:20px;">{{ item.title }}</h2>
                        <p style="color:grey;margin-left:20px;">{{ item.description }}</p>
                    </div>
                    <div class="task2" >

                        <p style="color:grey">9:30 A.M.</p>
                        <img src="../assets/profile pic.jpg" class="image">
                    </div>
                    
                     </div>

                     
           
                 </div>
                
          
        </div>

        <div style="padding: 30px;" >
                    <button @click="addtodoform" class="btn"> + Add new task</button>
                 </div>

   
  
</template>

<script>

export default{
  
    data(){
        return{
            tasks:[
                {title:"Project daily stand-up",description:"At the conference centre"},
            {title:"Internia new UI style",description:"Remember to bring presents"},
            {title:"Weekly review",description:"Wanda square E5"},
            {title:"Interview ",description:"Remember to bring laptop "},
                 ],
        showaddform:false,
        form:{title:"",description:""}

       


        }
   


    },
    methods :{

    addtodoform()
    {
       
       
        this.showaddform=true
       
    },

    savetodo(){
            console.log("hello")
            console.log(this.form)
            this.tasks.push(this.form)
            this.showaddform=false
        },

    closepopup(){


    //    if (this.showaddform ==true){
           this.showaddform=false
    //     }
        
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
    padding: 50px;
   
   
   
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
    }

.pop-up{
    
    background: pink;
    position: absolute;
    left: 40%;
    bottom: 35%;
    height: 400px;
    width: 400px;

    
    

}

.task2{
    margin-right: 20px;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.todoform{
    display: flex;
    flex-direction: column;
    align-items: center;
  
}
</style>


