<template>
    <div v-if="post !== null" class="section post">
        <article :class="{media: true, hot: isHot}">

            <figure class="media-left">
                <img :src="post.submissionImage" alt="submission image" class="image is-64x64">
            </figure>

            <div class="media-content">
                <div class="content">
                    <p>
                        <strong>
                            <strong class="has-text-primary">{{ post.title }}</strong>
                            <span class="tag is-small">#{{ post.id }}</span>
                        </strong>
                        <br>
                            {{ post.content }}
                        <br>
                        <small class="is-size-7">
                            
                        </small>
                    </p>
                </div>
<!--
                    <article class="media">
                        <figure class="media-left">
                            <p class="image is-48x48">
                            <img src="https://bulma.io/images/placeholders/96x96.png">
                            </p>
                        </figure>
                        <div class="media-content">
                            <div class="content">
                            <p>
                                <strong>Sean Brown</strong>
                                <br>
                                Donec sollicitudin urna eget eros malesuada sagittis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Aliquam blandit nisl a nulla sagittis, a lobortis leo feugiat.
                                <br>
                                <small><a>Like</a> · <a>Reply</a> · 2 hrs</small>
                            </p>
                            </div>
                        </div>
                    </article>    
-->
            </div>



            <div class="media-right">
                    <h3 class="has-text-primary">{{ post.votes }}<font-awesome-icon icon=chevron-up></font-awesome-icon></h3>
                    <button @click="increaseVotes()" class="button-primary">ME TOO</button>
            </div>

        </article>
    </div>
</template>

<script>
export default {
    props: {
        post: null
    },
    methods: {
        increaseVotes: function () {
            this.post.votes++;
        }
    },
    computed: {
        isHot: function () {
            return this.post.votes >= 20;
        }
    }
}
</script>


// STYLE
<style lang='scss' scoped>

.post p {
    font-size: calc(12px + 0.5vw);
}

.section {
    padding: 0.5rem 0.5rem;
}
.media {
    max-width: 1000px;
    margin: 0 auto;
    border: 2px solid #e6e7e9;
    padding: 1em 1.5em 0.5em 1.5em;
    border-radius: 0.3em;
}

.media-content{
    max-width: 700px;
}

.media-right{
    align-content: center;
}
// Once you reach 20 votes.
@mixin border-gradient($from, $to, $weight: 0) {
    $mix-main: mix($from, $to);
    $mix-sub-from: mix($mix-main, $from);
    $mix-sub-to: mix($mix-main, $to);

    box-shadow: 0 5px 0 $weight rgba($mix-sub-to, .25),
                0 -5px 0 $weight rgba($mix-sub-from, .25),
                5px 0 0 $weight rgba($mix-sub-to, .25),
                -5px 0 0 $weight  rgba($mix-sub-from, .25),
                5px -5px 0 $weight rgba($mix-main, .5),
                -5px 5px 0 $weight rgba($mix-main, .5),
                5px 5px 0 $weight rgba($to, .75),
                -5px -5px 0 $weight rgba($from, .75);
}
.hot {
    @include border-gradient(rgb(255, 72, 22), rgb(255, 185, 0));
}

</style>

<style scoped>
.button-primary{
    background-image: linear-gradient(45deg,#FD5A49,#FDDC98);
    border: white;
    color: white;
    font-size: 20px;
    padding: 10px;
    text-decoration: none;
    -webkit-transition-duration: 0.4s;
    transition-duration: 0.4s;
    cursor: pointer;
    font-family: 'Lato', sans-serif;
    text-align: center;
    border-radius: 5px;
}

.button-primary:hover {
    background-image:linear-gradient(225deg, #FD5A49,#FDDC98);
    color: white;
    border: 2px #FDDC98;
}

.has-text-primary{
    font-size: 25px;
}
</style>
