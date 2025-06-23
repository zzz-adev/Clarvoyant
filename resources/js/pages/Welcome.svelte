<script lang="ts">
    import { Link, page } from '@inertiajs/svelte';
    import AppLogoIcon from '@/components/AppLogoIcon.svelte';
    import HomeBanner from '@/components/HomeBanner.svelte';
    import HomeFeatures from '@/components/HomeFeatures.svelte';
    import HomeAppFlow from '@/components/HomeAppFlow.svelte';

    let user = $derived($page.props.auth.user);
</script>

<svelte:head>
    <title>Welcome</title>
    <link rel="preconnect" href="https://rsms.me/" />
    <link rel="stylesheet" href="https://rsms.me/inter/inter.css" />
</svelte:head>

<div class="flex min-h-screen flex-col items-center bg-[#FDFDFC] p-6 text-[#1b1b18] dark:bg-[#0a0a0a] lg:justify-center lg:p-8">
    <header class="not-has-[nav]:hidden mb-6 w-full max-w-[335px] text-sm lg:max-w-4xl">
        <nav class="flex items-center justify-between gap-4">
            <AppLogoIcon class="size-10 fill-current dark:text-white! text-black! bg-primary-foreground p-2 rounded" />
            {#if user}
                <Link
                    as="button"
                    href={route('dashboard')}
                    class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                >
                    Dashboard
                </Link>
            {:else}
                <Link
                    as="button"
                    href={route('login')}
                    class="inline-block rounded-sm border border-transparent px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#19140035] dark:text-[#EDEDEC] dark:hover:border-[#3E3E3A]"
                >
                    Log in
                </Link>
                <Link
                    as="button"
                    href={route('register')}
                    class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                >
                    Register
                </Link>
            {/if}
        </nav>
    </header>
    <div class="duration-750 starting:opacity-0 flex flex-col w-full
        items-start justify-center opacity-100 transition-opacity lg:grow max-w-[335px] text-sm lg:max-w-4xl">
        <HomeBanner />
        <HomeFeatures />
        <HomeAppFlow />
    </div>
    <div class="h-14.5 hidden lg:block"></div>
</div>
