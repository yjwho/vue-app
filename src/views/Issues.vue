<template>
<div class="issues">
<Issue name = "Jackie" issue="I called Alex white."/>
<Issue name = "Jackie" issue="Alex is white."/>
</div>
</template>

<script>
import Issue from "@/components/story.vue";

export default {
name: "issues",
components: {
Issue
}
};
</script>