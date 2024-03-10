<script lang="ts">
    import * as Card from "$lib/components/ui/card";
    import type { UserExperience } from "../routes/+page.svelte";
    export let userExp: UserExperience;
</script>


<div class="flex xl:mx-20 lg:mx-14 md:mx-10 sm:mx-8 mx-0 lg:flex-row flex-col justify-normal">
    <div class="justify-end flex lg:flex-row flex-col w-40 items-cente justify-centerr">
        <div class="my-2">
            <div class="flex justify-end">
                <img class="" src={userExp.companyIcon} alt="Link-external" width="36" height="36">
            </div>
            <div class="flex flex-col text-end">
                <span class="text-[16px] text-[#000000] font-bold">{userExp.companyName}</span>
                <span class="text-[12px] text-[#7A9299] font-normal">{userExp.location}</span>
                <span class="text-[12px] text-[#7A9299] font-normal">Joined</span>
                <span class="text-[12px] text-[#7A9299] font-normal">{userExp.joiningDate}</span>
            </div>
        </div>
        <img class="lg:rotate-0 rotate-90 max-lg:w-[12px] max-lg:ml-32" src="/experienceUserProfile.svg" alt="dottedLinedUserProfile" width="32" height="288">
    </div>
    
    <Card.Root class="lg:ml-6 px-6 mt-10 my-2 max-h-28 max-w-[600px]">
        <Card.Content class="flex flex-col">
            <span class="mt-2 text-[20px] text-[#141618] font-bold">
                {userExp.position}
            </span>
            <span class="mt-2 text-[#7A9299] text-[12px] font-normal">
                {userExp.Time}{userExp.remote? " · Remote" : ""}
            </span>
        </Card.Content>
    </Card.Root>
   
</div>
