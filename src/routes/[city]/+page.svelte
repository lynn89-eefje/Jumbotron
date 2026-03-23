<script>
    import { page } from "$app/state";
    import { base } from "$app/paths";
    import { onMount } from "svelte";
    import { eventName } from "$lib/event.js";

    onMount(() => {
        if (page.params.city == "live") {

        }
        else {
            window.location.href = base + "/" // Eventually should route to an error page
        }
    })

    let mode = $state(0);
</script>
<svelte:head>
    <title>Live Display | {eventName}</title>
</svelte:head>

<h1>Welcome to {eventName} Jumbotron</h1>