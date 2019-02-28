<template>
<div id="content" class="is-marginless is-paddingledd">
    <UpVote></UpVote>
</div>
</template>

<script>
import UpVote from "@/components/UpVote";

export default {
    name: "issues",
    components: {
        UpVote
    }
};
</script>

<style scoped>
#content{
    background: white;
    height: 100%;
}
</style>
