<template>
<div class = "container">
   <Searchbar @termChange="onTermChange"> </Searchbar>
   <div class ="row">
   <VideoDetail  v-bind:video="selectedVideo"></VideoDetail>
   <VideoList @selectedVideo="onVideoSelect" v-bind:videos="videos"> </VideoList>
   </div>
</div>
</template>

<script>
import axios from 'axios'
import Searchbar from './components/Searchbar'
import VideoList from './components/VideoList'
import VideoDetail from './components/VideoDetail'
const API_KEY = 'AIzaSyByCChAN8AqqufBxERBMOKgCgqZNHoLaPM'

export default {
    name: 'App',
    components: {
        Searchbar,
        VideoList,
        VideoDetail
    },
    data (){
        return {
            videos: [],
            selectedVideo: null
        }
    },
    methods: {
        onVideoSelect(video){
          this.selectedVideo = video

        },
        onTermChange (searchTerm) {
            axios.get('https://www.googleapis.com/youtube/v3/search', {
                params: {
                    key: API_KEY,
                    type: 'video',
                    part: 'snippet',
                    q: searchTerm
                }
            }).then(response => {
                this.videos = response.data.items
            })
        }
    }
}
</script>
 
 