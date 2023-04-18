<script>
  import socials from "$lib/assets/socials.json"
  let social = socials[0]

  import Names from '$lib/components/Names.svelte'
  import LinkedTitle from '$lib/components/DOI.svelte'

  import journals from '$lib/assets/journal_list.json'
  import briefs from '$lib/assets/brief_list.json'
  import confs from '$lib/assets/conf_list.json'
  import patents from '$lib/assets/patent_list.json'

</script>


<h1>
  Uroš Kalabić: Research works
</h1>

<a href={social.googlescholar} target="_blank">Google Scholar</a>


<h3>Journal papers</h3>

<ol>
{#each journals as journal}
  {#if journal.notes !== "submitted"}
    <li>
      <Names names={journal.names} />
      <br>"<LinkedTitle title={journal.title} doi={journal.doi}/>"
      <br><i>{journal.journal_title}</i>
      {#if journal.volume}<b>{journal.volume}</b>{/if}{#if journal.number}({journal.number}){/if}{#if journal.page_begin}&nbsp;{journal.page_begin}&ndash;{journal.page_end}{/if},
      {journal.date}
  {/if}
{/each}
</ol>

<h3>Brief communications</h3>

<ol>
{#each briefs as brief}
  {#if brief.notes !== "submitted"}
    <li>
      <Names names={brief.names} />
      <br>"<LinkedTitle title={brief.title} doi={brief.doi}/>"
      <br><i>{brief.journal_title}</i>
      {#if brief.volume}<b>{brief.volume}</b>{/if}{#if brief.number}({brief.number}){/if}{#if brief.page_begin}&nbsp;{brief.page_begin}&ndash;{brief.page_end}{/if},
      {brief.date}
    </li>
  {/if}
{/each}
</ol>

<h3>Conference proceedings</h3>

<ol>
  {#each confs as conf}
    {#if conf.notes !== "submitted"}
      <li>
        <Names names={conf.names} />
        <br>"<LinkedTitle title={conf.title} doi={conf.doi}/>"
        <br><i>{conf.conf_title}</i>{#if conf.number}&nbsp;({conf.number}){/if}{#if conf.page_begin}&nbsp;{conf.page_begin}&ndash;{conf.page_end}{/if},
        {conf.date} {#if conf.notes}[{conf.notes}]{/if}
      </li>
    {/if}
  {/each}
</ol>

<h3>Patents</h3>
<ol>
  {#each patents as patent}
    <li>
      <Names names={patent.names} />
      <br>"{patent.title}"
      <br><i>U.S. Patent {#if patent.patent}{patent.patent}{:else}Application {patent.patent_appl}{/if}</i>, filed {patent.filed}{#if patent.issued}&nbsp;& issued {patent.issued}{/if}
    </li>
  {/each}
</ol>
