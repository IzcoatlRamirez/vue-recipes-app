<template>

<v-container class="container-v">
    <v-img
    width="300"
    height="100"
    :src="image"
    cover></v-img>
    
    <v-card max-width="300"
        :title="title"
        :subtitle="culinaryCategory"
        :text="recipe"
        >
            <v-card-actions>
                <v-btn
                variant="tonal" 
                prepend-icon="mdi-delete-outline"
                class="btn">
                Delete
                </v-btn>
            </v-card-actions>

    </v-card>
</v-container>

</template>



<script setup>



defineProps({
  title : String,
  culinaryCategory: String,
  recipe : String,
  image : String

})
</script>



<style scoped>

.btn{
    background-color: #ff595e;
    color: white;
}

.container-v{
    max-width: 300px;
}

</style>