<script lang="ts">
    import Icon from "@iconify/svelte";
    const title = 'Simplify Your Contract Management';

    const subtitle = 'Stop losing track of important deadlines and contract terms. Clairvoyant gives you complete visibility and control over your legal documents.';
    const list = [
        'Upload and analyze contracts in seconds',
        'Ask natural language questions about your documents',
        'Get instant summaries of key terms and deadlines',
        'Set up automated reminders for renewals',
        'Track all contracts in one organized dashboard',
        'Highlight important clauses automatically',
        'Contract Analysis',
    ];
    const analysisPoints = [{
        id: 1,
        icon: 'ph:lightning-duotone',
        title: 'Key Point Detected',
        class: ['dark:bg-yellow-800/20 dark:text-yellow-100 dark:border-yellow-100 bg-yellow-100 text-yellow-600 border-yellow-600', 'dark:text-yellow-200 text-yellow-700'],
        description: 'Monthly retainer of $5,000',
    }, {
        id: 2,
        icon: 'ph:clock-countdown-duotone',
        title: 'Deadline Alert',
        class: ['dark:bg-green-800/20 dark:text-green-100 dark:border-green-100 bg-green-100 text-green-600 border-green-600', 'dark:text-green-200 text-green-700'],
        description: 'Contract renewal: December 31, 2024',
    },
    {
        id: 3,
        icon: 'ph:warning-duotone',
        title: 'Penalty Clause',
        class: ['dark:bg-red-800/20 dark:text-red-100 dark:border-red-100 bg-red-100 text-red-600 border-red-600', 'dark:text-red-200 text-red-700'],
        description: 'Late payment fee: 2% per month',
    }]
</script>

<main class="flex flex-col w-full overflow-hidden rounded-lg py-32
            lg:flex-col items-center bg-secondary/20">
    <div class="grid grid-cols-2 items-center justify-center w-full px-12">
        <div>
            <h1 class="text-xl text-primary font-extrabold pb-6">{title}</h1>
            <h2 class="text-primary pb-6">{subtitle}</h2>
            <ul>
                {#each list as item, id (id) }
                    <li class="flex gap-2 text-primary">
                        <Icon icon="ph:check-circle-duotone" class="w-6 h-6 mb-4 text-green-300" />
                        {item}
                    </li>
                {/each}
            </ul>
        </div>
        <div class="bg-primary-foreground p-6 mx-4 rounded-md shadow-2xl h-3/4">
            <h1 class="text-xl text-primary font-extrabold pb-6">Contract Analysis</h1>
            <ul>
            {#each analysisPoints as analysis (analysis.id)}
                <div class={["flex flex-col mb-3 p-2 rounded border w-full",
                    analysis.class[0]]}>
                    <div class="flex gap-2">
                        <Icon icon={analysis.icon} class="w-5 h-5" />
                        <p class="font-semibold">{analysis.title}</p>
                    </div>
                    <p class={analysis.class[1]}>{analysis.description}</p>
                </div>
            {/each}
            </ul>
        </div>
    </div>
</main>
