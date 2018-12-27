<template>
<ul class = "list-group col-md-4" >
<VideoListItem
 v-for="video in videos" 
 v-bind:video="video"
 :key="video.etag"
 @selectedVideo="onVideoSelect"
 > 
 </VideoListItem>
</ul>
</template>

<script>
import VideoListItem from './VideoListItem'

export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    methods:{
        onVideoSelect (video){
            this.$emit('selectedVideo', video)
        }
    },
    props: {
        videos: Array
    }
    
}
</script>

<style>

</style>
