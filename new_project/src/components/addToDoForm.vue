<template>
     <div class="todoform">
        <form style="    font-size: 20px;">
            <label>Title</label><br>
            <input v-model="form.title" type="text" ><br>
            <label>Description</label><br>
            <input v-model="form.description" type="text" ><br><br>
            
        </form>
        <button @click="savetodo">Save</button>
        
    </div>
</template>

<script>
export default{

    data(){
        return{
            form:{title:"",description:""}
        }
    },
    methods: {
        savetodo(){
            console.log("hello")
            console.log(this.form)
        }
    }
}
</script>