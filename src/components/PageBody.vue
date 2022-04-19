<template>
    <div>   
        <h1>Hello Assignment</h1>
        <PlayList/>
        <SongList class="songs" v-for="song in songs" 
            :key="song.id"
            :songArtist="song.songArtist"
            :songTitle="song.songTitle"
            :id="song.id"
            />
    </div>
</template>

<script>
import PlayList from "./PlayList.vue"
import SongList from "./SongList.vue"

    export default {
        name: 'PageBody',
        components: {
            PlayList,
            SongList
        },
        data() {
            return {
                songs: [
                    {
                        id: 1,
                        songArtist: "Jack Harlow",
                        songTitle: "First Class",
                    },
                    {
                        id: 2,
                        songArtist: "Harry Styles",
                        songTitle: "As Tt Was",
                    },
                    {
                        id: 3,
                        songArtist: "Glass Animals",
                        songTitle: "Heat Waves",
                    },
                    {
                        id: 4,
                        songArtist: "Latto",
                        songTitle: "Big Energy",
                    },
                    {
                        id: 5,
                        songArtist: "Imagine Dragons X JID",
                        songTitle: "Enemy",
                    },
                    {
                        id: 6,
                        songArtist: "The Kid LAROI",
                        songTitle: "Stay",
                    },
                    {
                        id: 7,
                        songArtist: "Kodak Black",
                        songTitle: "Super Gremlin",
                    },
                    {
                        id: 8,
                        songArtist: "Doja Cat",
                        songTitle: "Woman",
                    },
                    {
                        id: 9,
                        songArtist: "GAYLE",
                        songTitle: "abcdefu",
                    },
                    {
                        id: 10,
                        songArtist: "Ed Sheeran",
                        songTitle: "Bad Habits",
                    }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
div{
    position: relative;
    display: grid;
    grid-template-columns: 1fr 1fr;
    h1{
        grid-row-start: 1;
        grid-column-start: 2;
    }
    
    
}


</style>