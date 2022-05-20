<script>
    import Card from "./Card.svelte";
    import { onMount } from "svelte";
    import { Pulse } from "svelte-loading-spinners";

    export let name;

    let repos;
    onMount(async () => {
        try {
            const response = await fetch(`https://api.github.com/users/${name}/repos`, {method: "GET"});
            const data = await response.json();

            repos = data;

        } catch (e) {
            console.log(e);
        }
    });

</script>

<Card>
{#if repos !== undefined}
    <div class="p-8 flex flex-col gap-[3em]">
        {#each repos as repo}
            <Card>
                <div class="p-8 flex flex-col gap-2">
                    <a href={repo["html_url"]}> <h4>{repo["name"]}</h4> </a>
                    <p>{repo["description"] !== null ?  repo["description"] : "No description"}</p>
                </div>
            </Card>
        {/each}
    </div>
{:else}
    <div class="rounded-xl shadow-xl w-full p-2 flex flex-row duration-200 bg-gray-600/30 hover:bg-gray-500/30">
        <div class="mx-auto">
            <Pulse color="#e5e7eb" />
        </div>
    </div>
{/if}
</Card>