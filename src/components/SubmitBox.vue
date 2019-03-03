<template>
    <div class="section post">
        <b-button v-b-toggle.collapse3 class="m-1">RECORD MY EXPERIENCE</b-button>
        <b-collapse id="collapse3">
        <br>

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
        </b-collapse>
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
            var today = new Date();
            var date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
            var time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
            var dateTime = date+' '+time;

            var post = {
                title: this.title,
                content: this.content,
                // TODO: create login system and set up below fields.
                url: "#",
                time: dateTime,
                avatar: "./images/avatars/daniel.jpg",
                submissionImage: "./images/submissions/image-yellow.png"
            }
            // create post.
            this.$emit('submittedPost', post);

            this.title = '';
            this.content = '';

            //collapse the collapsable button
            this.$root.$emit('bv::toggle::collapse', 'collapse3')
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
        background-image:linear-gradient(45deg, rgb(132, 195, 196),rgb(68, 57, 172));
        color: white;
        border: 2px #7062F0;
    }

    .m-1:hover {
    background-image:linear-gradient(45deg, rgb(132, 195, 196),rgb(68, 57, 172));
    color: white;
    border: 4px #7062F0;
    }

    .m-1 {
        float:initial;
        border-radius: 4px;
    }
</style>
