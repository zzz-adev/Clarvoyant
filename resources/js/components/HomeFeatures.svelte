<script lang="ts">
    import Icon from "@iconify/svelte";
    const features: { title: string; description: string, icon: string, id: string }[] = [
        {
            title: 'AI-Powered Analysis',
            description: 'Automatically extract key points, deadlines, and risks from your contracts',
            icon: 'ph:brain-duotone',
            id: 'ai-analysis'
        },
        {
            title: 'Smart Reminders',
            description: 'Never miss important deadlines with intelligent notification system',
            icon: 'ph:clock-countdown-duotone',
            id: 'smart-reminders'
        },
        {
            title: 'Visual Contract Review',
            description: 'Highlighted clauses and color-coded tags for quick scanning',
            icon: 'ph:eye-duotone',
            id: 'visual-review'
        },
        {
            title: 'Risk Detection',
            description: 'Identify potential penalties and obligations before they become problems',
            icon: 'ph:shield-duotone',
            id: 'risk-detection'
        }
    ]
</script>

<main class="flex flex-col w-full overflow-hidden rounded-lg py-32
                    lg:flex-col items-center text-center">
    <h1 class="text-4xl text-primary font-extrabold pb-6">Everything You Need to Manage Contracts</h1>
    <p class="text-xl text-primary pb-12">From upload to analysis to reminders, Clairvoyant handles every aspect of contract management.</p>
    <div class="grid grid-cols-2 lg:grid-cols-4 text-center place-items-start gap-6">
        {#each features as feature (feature.id)}
            <div class="flex flex-col items-center text-center border p-2 h-full w-full justify-between hover:shadow-lg transition-shadow rounded-md">
                <Icon icon={feature.icon} class="w-12 h-12 mb-4 text-accent bg-accent/10 p-2 rounded" />
                <h2 class="text-xl text-primary font-bold">{feature.title}</h2>
                <p class="text-base text-primary">{feature.description}</p>
            </div>
        {/each}
    </div>
</main>
