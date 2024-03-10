<script lang="ts">
    import * as Card from "$lib/components/ui/card";
    import type { UserArticle } from "../routes/+page.svelte";
    export let articles: UserArticle;
</script>

<Card.Root class="xl:ml-6 my-2 min-h-48 min-w-[334px]">
    <Card.Header>
        <img class="h-[136px] w-full rounded-sm" 
        src={articles.articleImage} 
        alt="userImage" width="120" height="120">
    </Card.Header>
    <Card.Content class="truncate w-full px-6">
        <span >
           {articles.articleContent}
        </span>
    </Card.Content>
</Card.Root>
