<script lang="ts">
    import ArticleCard from "$lib/articleCard.svelte";
    import type { ArticleArray } from "../routes/+page.svelte";
    export let userArticles: ArticleArray;
</script>

<div class="xl:mx-20 lg:mx-14 md:mx-10 sm:mx-8 mx-0 max-lg:mt-5">
  <div class="flex justify-between">
    <div class="flex lg:flex-row flex-col items-center h-fit">
        <div class="w-40 lg:justify-end flex lg:flex-row flex-col items-center">
            <div class="flex justify-center pt-1 text-[15px] text-[#7A9299] font-normal items-center">
            {userArticles.date}
            </div>
            <img class="lg:rotate-0 rotate-90 max-lg:h-10" src="/articleUserProfile.svg" alt="dottedLinedUserProfile">
        </div>
        <div class="lg:mt-10 mt-0">
            <div class="w-fit flex lg:flex-row flex-col overflow-x-auto">
                {#each userArticles.articles as article}
                    <ArticleCard articles={article}/>
                {/each}
            </div>
        </div>
    </div>
  </div>
</div>