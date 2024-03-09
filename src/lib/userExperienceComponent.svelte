<script lang="ts">
    import * as Card from "$lib/components/ui/card";
    import type { UserExperience } from "../routes/+page.svelte";
    export let userExp: UserExperience;
</script>


<div class="flex mx-20 justify-normal">
    <div class="justify-end flex w-40 items-center">
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
        <img src="/experienceUserProfile.svg" alt="dottedLinedUserProfile" width="32" height="288">
    </div>
    
    <Card.Root class="ml-6 px-6 mt-10 max-h-20 min-w-[600px] ">
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
