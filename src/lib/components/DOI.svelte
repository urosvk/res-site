<script>
	export let title;
    export let doi;

    let link = "https://" + doi;
</script>

{#if doi}
    <a href={link} target="_blank">{title}</a>
{:else}
    {title}
{/if}