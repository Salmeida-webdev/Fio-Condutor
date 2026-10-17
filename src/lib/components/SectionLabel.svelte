<script lang="ts">import type { Snippet } from 'svelte'; let {index, children}: {index:string;children:Snippet} = $props();</script>
<div class="section-label"><span>{index}</span><span class="rule"></span><span>{@render children()}</span></div>
<style>.section-label{display:flex;align-items:center;gap:.75rem;color:var(--ink-soft);font:500 .66rem 'IBM Plex Mono',monospace;letter-spacing:.12em;text-transform:uppercase}.section-label>span:first-child{color:var(--coral)}.rule{width:2rem;height:1px;background:var(--coral)}</style>
