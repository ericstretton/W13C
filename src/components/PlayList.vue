<template>
    <div>
        <h1>Playlist</h1>
        <div>{{clickedChikd}}</div>
        <SongList v-bind:class="songAdded" v-for="song in songs" 
            :key="song.id"
            :songArtist="song.songArtist"
            :songTitle="song.songTitle"
            :id="song.id"
            />
    </div>
</template>

<script>
import SongList from "./SongList.vue"

    export default {
        name: 'PlayList',
        components: {
            SongList,
        },
        data() {
            return {
                
            }
        },
        methods: {
            handleChildUpdate(songAdded) {
                this.clickedChild = songAdded;
                console.log(songAdded);
            }
        },

    }
</script>

<style lang="scss" scoped>


</style>