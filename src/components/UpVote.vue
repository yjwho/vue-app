<template>
    <div>
        <br>
        <br>
        <br>
        <div class="section header">
            <h2 class="title has-text-centered dividing-header">OUR STORIES</h2>
        </div>

    <div>


    </div>
        <div class="content">
            <br>
            <SubmitBox @submittedPost="createPost"></SubmitBox>
            <Post v-for="a in sortedSubmissions" :post="a" :key="a.id"></Post>
        </div>

        <footer class="footer"></footer>
    </div>
</template>

<script>
import Post from '@/components/Post'
import SubmitBox from '@/components/SubmitBox'
import seed from '@/seed.json'

export default {
    components: {
        Post,
        SubmitBox
    },
    data: function () {
        return {
            submissions: seed.posts
            }
    },
    computed: {
        sortedSubmissions: function () {
            return this.submissions.slice(0).sort( (a,b) => {
                return b.votes - a.votes;
            });
        },
        numSubmissions: function () {
            return this.submissions.length;
        }
    },
    methods: {
        createPost: function (post) {
            post.votes = 0;
            post.id = this.numSubmissions + 1;
            this.submissions.push(post);
        }
    }
}
</script>


// STYLE
<style scoped>

.header {
    padding: 3rem 1rem 1.5rem;
}

.footer {
    padding: 2rem;
    background-color: #484C91;
}

h2{
    font-size: 50px;
    font-family: 'Lato', sans-serif;
    color: #3D3949;
}

button{
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
    border-radius: 5px;
}

</style>