<script lang="ts">
  import type { UserData } from "../routes/+page.svelte";
  import { Button } from "./components/ui/button";
  export let userData: UserData;
</script>

<div class="xl:mx-40 lg:mx-20 md:mx-14 sm:mx-10 mx-5 py-2 mt-20 flex xl:flex-row flex-col justify-between">
    <div class="flex flex-col items-center">
        <div class="w-32">
            <img class="rounded-full border-[5px]border-[#EAEFF5]" src="/userImage.svg" alt="userImage" width="120" height="120">
        </div>
        <div class="text-3xl w-32 text-center justify-center font-bold text-[#4B5C6D]">
            {userData.userName}
        </div>
    </div>

    <div class="flex flex-col mx-10 my-2">
        <div class="flex lg:flex-row flex-col items-center">
            <div class="my-2 2xl:max-w-fit ">
                {userData.about}
            </div>
            
            <div class="my-2 ml-10">
                <div class="flex justify-end">
                    <img class="right-0" src={userData.currentCompanyIcon} alt="Link-external" width="36" height="36">
                </div>
                <div class="flex flex-col text-end">
                    <span class="text-[16px] text-[#000000] font-bold">{userData.currentCompany}</span>
                    <span class="text-[12px] text-[#7A9299] font-normal">{userData.currentPosition}</span>
                </div>
            </div>
        </div>
        <div class="flex justify-between mt-5">
            <Button variant="shadowButton" class="h-8 ml-3">Follow</Button>
            <div class="flex">
                <a href={userData.websiteLink} class="flex" target="_blank">
                    <span class="text-[#4D4D4D] text-sm font-normal">My Website</span> 
                    <img class="mx-1 mb-2" src="/link-external.svg" alt="Link-external" width="12" height="12">
                </a>
                <img class="mx-1 mb-2" src=" /dot-horizontal.svg" alt="Link-external" width="16" height="16">
            </div>
        </div>
    </div>
</div>