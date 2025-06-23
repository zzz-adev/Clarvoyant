<script lang="ts">
    import { SidebarGroup, SidebarGroupContent, SidebarMenu, SidebarMenuItem } from '@/components/ui/sidebar';
    import { Slider } from '@/components/ui/slider';

    interface Props {
        class?: string;
    }

    let { class: className }: Props = $props();
    const totalStorage = 5;
    const usedStorage = 2.1;
</script>

<SidebarGroup class="group-data-[collapsible=icon]:p-0 {className}">
    <SidebarGroupContent>
        <SidebarMenu>
                <SidebarMenuItem>
                    <div>
                        <p class="font-semibold">Storage Used</p>
                        <div class="flex gap-2 text-primary text-xs">
                            <Slider disabled class="disabled pointer-none w-4/6" type="single" min={0} max={totalStorage} value={usedStorage} step={0.1} />
                            <p class="font-semibold">{usedStorage} / {totalStorage} GB</p>
                        </div>
                    </div>
                </SidebarMenuItem>
        </SidebarMenu>
    </SidebarGroupContent>
</SidebarGroup>
