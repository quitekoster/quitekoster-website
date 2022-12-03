<script lang="ts">
    import { page } from "$app/stores";
    import { each } from "svelte/internal";

    const links: {link: string, title: string}[] = [
        { link: '/', title: 'About Me' },
        { link: '/resume', title: 'Resume' },
        { link: '/projects', title: 'Projects' },
        { link: '/blog', title: 'Blog' },
    ]
</script>

<nav class="bg-white ">
    <div class="flex flex-wrap justify-between items-center mx-auto max-w-screen-xl px-4 md:px-6 py-2.5">
        <a href="https://flowbite.com" class="flex items-center">
            <span class="self-center text-xl font-semibold whitespace-nowrap ">Christopher Koster</span>
        </a>
        <div class="flex items-center">
            <a href="mailto:christopher@quitekoster.com" class="mr-6 text-sm font-medium text-gray-500 hover:underline">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.928 5.493a3 3 0 01-3.144 0L1.5 8.67z" />
                    <path d="M22.5 6.908V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.158l9.714 5.978a1.5 1.5 0 001.572 0L22.5 6.908z" />
                </svg>                
            </a>
        </div>
    </div>
</nav>
<nav class="sticky top-0 shadow z-20 bg-white border-gray-800 border-b-2">
    <div class="max-w-screen-xl px-4 py-3 mx-auto md:px-6">
        <div class="flex items-center">
            <ul class="flex flex-row mt-0 mr-6 space-x-8 text-sm font-medium">
                {#each links as link }
                    <li>
                        <a href="{link.link}" class:border-b-4={$page.route.id === link.link} class="text-gray-900 uppercase border-b-red-600 hover:border-b-4 hover:border-b-blue-600">{link.title}</a>
                    </li>
                {/each}
            </ul>
        </div>
    </div>
</nav>

  