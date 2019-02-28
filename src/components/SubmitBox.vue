<template>
    <div class="section post">
        <article class="media">

            <figure class="media-left">
                <p class="image is-64x64">
                    <img src="@/../public/images/avatars/molly.png">
                </p>
            </figure>

            <div class="media-content">
                <div class="content">
                    <div class="field">
                        <div class="control">
                            <input class="input" type="text" placeholder="Post title." v-model="title">
                        </div>
                    </div>
                    <div class="field">
                        <p class="control">
                            <textarea class="textarea" placeholder="Post body." v-model="content"></textarea>
                        </p>
                    </div>
                    <div>
                        <button @click.prevent="submitPost()" class="button is-info">Submit</button>
                        
                    </div>
                </div>
            </div>

        </article>
    </div>
</template>

<script>
export default {
    data: function () {
        return {
            title: '',
            content: ''
        }
    },
    methods: {
        submitPost: function () {
            var post = {
                title: this.title,
                content: this.content,
                // TODO: create login system and set up below fields.
                url: "#",
                avatar: "./images/avatars/daniel.jpg",
                submissionImage: "./images/submissions/image-yellow.png"
            }
            // create post.
            this.$emit('submittedPost', post);

            this.title = '';
            this.content = '';
        }
    }
};
</script>

<style lang="scss" scoped>

.section {
    padding: 0.5rem 0.5rem;
}

.media {
    max-width: 1000px;
    margin: 0 auto;
    border: 1px solid #e6e7e9;
    padding: 1em 1.5em 0.5em 1.5em;
    border-radius: 0.3em;
}

</style>

<style scoped>
    button{
        float: right;
        background-image: linear-gradient(45deg,#ABE5E6,#7062F0);
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
    }

    .button:hover {
        background-image:linear-gradient(225deg, #ABE5E6,#7062F0);
        color: white;
        border: 2px #7062F0;
    }
</style>
