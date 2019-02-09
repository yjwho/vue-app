<template>
    <div>
        <h1 id="issue-title">Issues</h1>
        <h2 id="issue-name">{{ nameTitle }}</h2>
        <p>{{name}}</p>
        <h2 id="issue-name">{{issueTitle}}</h2>
        <p>{{issue}} - Len: {{issueLength}}</p>
        <button v-if="showButton" v-on:click="toggleShowButton()">Me too!</button>
    </div>
</template>

<script>
export default {
    name: "Issue",
    props: {
        name: {
            type: String,
            default: "missing name"
        },
        issue: {
            type: String,
            default: "Missing details"
        }
    },
    data() {
        return {
            //data that is static

            showButton: true,
            nameTitle: "Name Title",
            issueTitle: ""
        }
    },
    computed: {
        issueLength() { 
            //a custom function designed to return data
            //it will recompute if data is changed
            //return the length of issue in props
            return this.issue.length;
        }
    },
    methods:{
        toggleShowButton(){
            this.showButton = !this.showButton;
        }
    },
    mounted(){
        //API calls
        this.issueTitle = "Issue"
    }
}
</script>

<style>
/* everythin under here only applies to this
template component */
#issue-title {
    color: green;
}
</style>
