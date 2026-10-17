<script lang="ts">let { compact = false, inverse = false }: {compact?: boolean; inverse?: boolean} = $props();</script>
<a class:compact href="/" class:inverse aria-label="Fio Condutor Tecnologia — início">
  <svg class="mark" viewBox="0 0 48 48" aria-hidden="true">
    <path d="M8 10h25a7 7 0 0 1 0 14H17a7 7 0 0 0 0 14h23" />
    <circle cx="8" cy="10" r="3.5" /><circle cx="40" cy="38" r="3.5" />
  </svg>
  {#if !compact}<span class="wordmark"><strong>fio condutor</strong><small>TECNOLOGIA</small></span>{/if}
</a>
<style>
  a{display:inline-flex;align-items:center;gap:.68rem;color:var(--ink);text-decoration:none}.mark{width:42px;height:42px;overflow:visible}.mark path{fill:none;stroke:var(--coral);stroke-width:2.6;stroke-linecap:round}.mark circle{fill:var(--coral)}.wordmark{display:grid;line-height:1}.wordmark strong{font:700 1.04rem/1.05 'Syne',sans-serif;letter-spacing:-.055em}.wordmark small{font:500 .52rem/1.8 'IBM Plex Mono',monospace;letter-spacing:.2em}.inverse{color:var(--paper)}
</style>
