<template>
    <div class="category_wrap px-7 py-3 h-screen">
        <div class="category_title">
            <p class="text-primary font-medium text-sm ma-0 pa-0 ">Popular Category</p>
            <div class="relative gap-2 flex align-center">
                <p class="font-bold   ma-0 pa-0">Popular Category For Learning</p>
                <select placeholder="kndslld">
                    <option v-for="(items,index) in categoryItems" :value="items" :key="index">{{items}} <v-icon>mdi-account</v-icon> </option>
                </select>
            </div>
           

        </div>
    </div>
</template>

<script>
export default {
    name: "MinCategory",
  
    data:()=>({
        categoryItems: ['Degrees', 'Course', 'Cohorts', 'Specialization'],
    })

}
</script>

<style scoped>
select{
    outline: none;
    border-bottom: 1px solid #60109E;
    color: black;
    padding: 0 0;
}

</style>