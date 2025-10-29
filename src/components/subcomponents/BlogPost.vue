<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        props: {
            subject: String,
            entry: String,
            mood: String
        },
        computed: {
            imageUrl() {
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card --> 
    <div class="card mb-4" style="width: 20rem;">
        <div class="card-body">
            <img class="img-fluid" :src="imageUrl"/>
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}</p>
            <slot></slot>
        </div>
    </div>

</template>

