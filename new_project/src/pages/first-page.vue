<template>
    

        <div class="container">
            <div class="content">
                <h1>Today</h1>
                <p style="color:grey;">18th June 2019,Tuesday</p>

                <div v-for= "item in tasks" class="task">
                <h2>{{ item.title }}</h2>
                <p style="color:grey">{{ item.description }}</p>
                </div>
            </div>
        </div>

   
  
</template>

<style scoped>
.container{
    background:rgb(222, 193, 140);
    
    
}

.content{
    background:white;
    border-radius:10px;
    margin:20px;
   
   
   
}

.task{
    background:white;
    border-radius:20px;
    border:1px solid grey;
    margin-top:10px;
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