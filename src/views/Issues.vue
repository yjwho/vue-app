<template>
<!--
<div class="issues">
<Issue name = "Jackie" issue="I called Alex white."/>
<Issue name = "Jackie" issue="Alex is white."/>
</div>
 -->
<div id="app" class="is-marginless is-paddingledd">
    <UpVote></UpVote>
</div>
</template>

<script>
//import Issue from "@/components/story.vue";
import UpVote from "@/components/UpVote";

export default {
    name: "issues",
    components: {
        //Issue
        UpVote
    }
};
</script>