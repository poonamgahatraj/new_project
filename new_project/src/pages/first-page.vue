<template>
    

        <div class="container">
           
                <div class="content">
                    <div>
                        <h1 style="margin-left: 20px;;">Today</h1>
                        <p style="color:grey;margin-left: 20px;">18th June 2019,Tuesday</p>
                    </div>
                

                    <div v-for= "item in tasks" class="task">
                    <div>
                        <h2 style="margin-left:20px;">{{ item.title }}</h2>
                        <p style="color:grey;margin-left:20px;">{{ item.description }}</p>
                    </div>
                    <div >
                        <img src="../assets/profile pic.jpg" class="image">
                    </div>
                    
                     </div>

                     
           
                 </div>
           <button class="btn"> + Add new task</button>
        </div>

   
  
</template>

<style scoped>
.container{
    background:rgb(222, 193, 140);
    border:1px solid rgb(222, 193, 140);
    
    
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
    margin-top: 10px;
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
    font-size: 18px;
}

.image{
    height: 25px;
    width: 25px;
    border-radius: 25px;
    margin-right: 20px;
}
</style>

<script>
export default{
    data(){
        return{
            tasks:[{title:"Project daily stand-up",description:"At the conference centre"},
            {title:"Internia new UI style",description:"Remember to bring presents"},
            {title:"Weekly review",description:"Wanda square E5"},
            {title:"Interview ",description:"Remember to bring laptop "}
        
        ]
        }

    }
}
</script>