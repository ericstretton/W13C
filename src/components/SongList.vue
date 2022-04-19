<template>
    <div @click="notifyParent">
        <div>
        <h2>{{songArtist}}</h2>
        <h3>{{songTitle}}</h3>
        </div>
        <button v-on="click">Add to Play List</button>
    </div>
</template>

<script>
    export default {
        name: 'SongList',
        props: {
            id : Number,
            songArtist : String,
            songTitle : String,
        },
        methods: {
            notifyParent(){
                this.$emit('childClicked', this.postContent);
                this.$root.$emit('childSong', this.id);
            },
            updateSong(songId){
                if(this.id ==songId){
                    this.clicked = true;
                }else{
                    this.clicked = false;
                }
            }
        },
        mounted () {
            this.$root.$on('childSong', this.updateSong);
        },
    }
</script>

<style lang="scss" scoped>

div{
border: black solid 2px;
width: 30vw;
grid-column: 2;
height: 10vh;
}

button{
    position: absolute;
    left: 0vw;
    bottom: 0vw;
}

</style>