<script>
    import { Drawer, CloseButton, Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    import { ChartPieSolid, GridSolid, MailBoxSolid, UsersSolid } from 'flowbite-svelte-icons';
    import { sineIn } from 'svelte/easing';
    let hidden2 = true;
    let spanClass = 'flex-1 ms-3 whitespace-nowrap';
    let transitionParams = {
        x: -320,
        duration: 200,
        easing: sineIn
    };
</script>

<div class="text-center">
    <div on:click={() => (hidden2 = false)}>
        <img src="https://img.icons8.com/ios-filled/30/ffffff/menu--v1.png" alt="/" class="h-6 w-6 sm:mx-32 sm:mx-12 mx-8 sm:mt-12 mt-8"/>
    </div>
</div>
<Drawer transitionType="fly" {transitionParams} bind:hidden={hidden2} id="sidebar2" class="rounded-md bg-gradient-to-b from-orange-500/90 to-black !important">
    <div class="flex items-center">
        <h5 id="drawer-navigation-label-3" class="text-base font-semibold text-gray-200 uppercase dark:text-gray-400">Menu</h5>
        <CloseButton on:click={() => (hidden2 = true)} class="mb-4 dark:text-white" />
    </div>
    <Sidebar>
        <SidebarWrapper divClass=" overflow-y-auto py-4 px-3 rounded">
            <SidebarGroup>
                <SidebarItem label="Download" class="font-semibold text-white hover:bg-black hover:text-white hover:no-underline">
                    <svelte:fragment slot="icon">
                        <ChartPieSolid class="w-5 h-5 text-gray-200 transition duration-75 dark:text-gray-200 group-hover:text-gray-200 dark:group-hover:text-white" />
                    </svelte:fragment>
                </SidebarItem>
                <SidebarItem label="Documentation" class="font-semibold text-white hover:bg-black hover:text-white hover:no-underline" {spanClass}>
                    <svelte:fragment slot="icon">
                        <GridSolid class="w-5 h-5 text-gray-200 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
                    </svelte:fragment>
                </SidebarItem>
                <SidebarItem label="Agni OS" class="font-semibold text-white hover:bg-black hover:text-white hover:no-underline" {spanClass}>
                    <svelte:fragment slot="icon">
                        <MailBoxSolid class="w-5 h-5 text-gray-200 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
                    </svelte:fragment>
                </SidebarItem>
                <SidebarItem label="About us" class="font-semibold text-white hover:bg-black hover:text-white hover:no-underline">
                    <svelte:fragment slot="icon">
                        <UsersSolid class="w-5 h-5 text-gray-200 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white" />
                    </svelte:fragment>
                </SidebarItem>
            </SidebarGroup>
        </SidebarWrapper>
    </Sidebar>
</Drawer>
