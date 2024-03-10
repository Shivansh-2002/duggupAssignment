<script lang="ts">
  export let userData: UserData;

  import { Button } from "$lib/components/ui/button";
  import * as DropdownMenu from "$lib/components/ui/dropdown-menu";
  import type { UserData } from "../routes/+page.svelte";

</script>

<header class="xl:mx-24 z-50 bg-[#FCFCFF] fixed top-0 left-0 right-0 py-2 flex justify-between items-center border-b-[1px] border-dotted  border-gray-400 border-opacity-100">
  
  <div class="flex items-center xl:ml-0 ml-3">
    <img src="/logoIcon.svg" alt="Logo" width="27" height="28">
    <h1 class="text-[21px] ml-1 font-bold text-gray-700"> duggup</h1>
  </div>

  <div class="flex items-center space-x-4">
   
    <a href="/" class="hover:text-gray-300 text-sm flex max-lg:hidden">
      <img src="/homeIcon.svg" alt="Logo" width="22" height="22">
      Home
    </a>
   
    <a href="/" class="hover:text-gray-300 text-sm flex max-lg:hidden">
      <img src="/exploreIcon.svg" alt="Logo" width="22" height="22">
      Explore
    </a>
   
    <a href="/" class="hover:text-gray-300 text-sm flex max-lg:hidden">
      <img src="/learnIcon.svg" alt="Logo" width="22" height="20">
      Learn
    </a>
   
    <Button 
      variant="shadowButton" 
      class="w-[80px] text-[#4D4D4D] gap-1 max-lg:hidden"   
      size="shadowButton"
    >
      <img src="/plus-square.svg" alt="Logo" width="16" height="16">
      Post
    </Button>

    <DropdownMenu.Root>
      <DropdownMenu.Trigger>
        <div class="flex xl:mr-0 mr-3">
          <img class="rounded-full border-[0.5px] border-[#4D4D4D]" src="/userImage.svg" alt="userImage" width="40" height="40">
          <span class="truncate max-w-40 text-[#4D4D4D] text-lg mx-2 mt-[6px]">{userData.userName}</span>
           <img class="mt-1" src="/chevron-down.svg" alt="Logo" width="16" height="16">
        </div>
      </DropdownMenu.Trigger>
      <DropdownMenu.Content>
        <DropdownMenu.Group>
          <DropdownMenu.Label>My Account</DropdownMenu.Label>
          <DropdownMenu.Separator />
          <DropdownMenu.Item class="lg:hidden">
            Home
          </DropdownMenu.Item>
          <DropdownMenu.Item class="lg:hidden">
            Explore
          </DropdownMenu.Item>
          <DropdownMenu.Item class="lg:hidden">
            Learn
          </DropdownMenu.Item>
          <DropdownMenu.Item class="lg:hidden">
            Post</DropdownMenu.Item>
          <DropdownMenu.Item>Profile</DropdownMenu.Item>
          <DropdownMenu.Item>Team</DropdownMenu.Item>
          <DropdownMenu.Item>Subscription</DropdownMenu.Item>
          <DropdownMenu.Item>Logout</DropdownMenu.Item>
        </DropdownMenu.Group>
      </DropdownMenu.Content>
    </DropdownMenu.Root>
  </div>
</header>