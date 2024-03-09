<script lang="ts">
    import ArticleCard from "$lib/articleCard.svelte";
    import type { ArticleArray } from "../routes/+page.svelte";
    export let userArticles: ArticleArray;
</script>

<div class="mx-20">
  <div class="flex justify-between">
    <div class="flex">
        <div class="w-40 justify-end flex items-center">
            <div class="flex justify-center pt-1 h-full text-[15px] text-[#7A9299] font-normal items-center">
            {userArticles.date}
            </div>
            <img class="" src=" /articleUserProfile.svg" alt="dottedLinedUserProfile" width="32" height="288">
        </div>
        <div class="mt-10">
            <div class="w-[900px] flex overflow-x-auto">
                {#each userArticles.articles as article}
                    <ArticleCard articles={article}/>
                {/each}
            </div>
        </div>
    </div>
  </div>
</div>