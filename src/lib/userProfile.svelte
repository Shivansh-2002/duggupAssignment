<script lang="ts">
  import { Button } from "./components/ui/button";
  export let userName: string;
</script>

<div class="mx-36 py-2 mt-10 flex justify-center">
    <div>
        <div class="w-32">
            <img class="rounded-full border-[5px]border-[#EAEFF5]" src="/userImage.svg" alt="userImage" width="120" height="120">
        </div>
        <div class="text-3xl w-32 text-center justify-center font-bold text-[#4B5C6D]">
            {userName}
        </div>
    </div>

    <div class="flex flex-col mx-10 my-2">
        <div class="flex justify-between">
            <div class="my-2 max-w-[620px]">
                Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.
            </div>
            
            <div class="my-2 ml-10">
                <div class="flex justify-end">
                    <img class="right-0" src="/duggupLogo.svg" alt="Link-external" width="36" height="36">
                </div>
                <div class="flex flex-col text-end">
                    <span class="text-[16px] text-[#000000] font-bold">Duggup</span>
                    <span class="text-[12px] text-[#7A9299] font-normal">Co-Founder and CEO</span>
                </div>
            </div>
        </div>
        <div class="flex justify-between mt-5">
            <Button variant="shadowButton" class="h-8 ml-3"> Follow</Button>
            <div class="flex">
                <a href="https://www.krishnakiran.com/" class="flex" target="_blank">
                    <span class="text-[#4D4D4D] text-sm font-normal">My Website</span> 
                    <img class="mx-1 mb-2" src="/link-external.svg" alt="Link-external" width="12" height="12">
                </a>
                <img class="mx-1 mb-2" src=" /dot-horizontal.svg" alt="Link-external" width="16" height="16">
            </div>
        </div>
    </div>
</div>