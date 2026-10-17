<script lang="ts">
  import { onMount } from 'svelte';
  import Mark from './Mark.svelte';
  const links = [{href:'/solucoes',label:'Soluções'},{href:'/demonstracoes',label:'Demonstrações'},{href:'/processo',label:'Como trabalhamos'},{href:'/insights',label:'Insights'}];
  let menuOpen = $state(false);
  let enhanced = $state(false);
  onMount(() => { enhanced = true; });
</script>
<a class="skip" href="#conteudo">Pular para o conteúdo</a>
<header class="site-header">
  <div class="header-inner"><Mark />
    <button class="menu-toggle" aria-expanded={menuOpen} aria-controls="menu-principal" onclick={() => menuOpen = !menuOpen}>
      <span>{menuOpen ? 'Fechar' : 'Menu'}</span><span class="menu-icon" aria-hidden="true">{menuOpen ? '−' : '+'}</span>
    </button>
    <nav id="menu-principal" class:enhanced class:open={menuOpen} aria-label="Navegação principal">
      {#each links as link}<a href={link.href} onclick={() => menuOpen = false}>{link.label}</a>{/each}
      <a class="nav-contact" href="/contato" onclick={() => menuOpen = false}>Vamos conversar <span aria-hidden="true">↗</span></a>
    </nav>
  </div>
</header>
<style>
  .site-header{position:sticky;top:0;z-index:20;background:color-mix(in srgb,var(--paper) 93%,transparent);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}.header-inner{max-width:1320px;margin:auto;padding:.85rem clamp(1.1rem,5vw,4rem);display:flex;align-items:center;justify-content:space-between;gap:2rem}.site-header nav{display:flex;align-items:center;gap:clamp(1rem,2.6vw,2.7rem)}nav a{font-size:.82rem;color:var(--ink-soft);text-decoration:none;transition:color .2s}nav a:hover,nav a:focus-visible{color:var(--coral)}nav .nav-contact{color:var(--ink);font-weight:700;border-bottom:1px solid var(--coral);padding:.55rem 0}.nav-contact span{color:var(--coral);margin-left:.35rem}.menu-toggle{display:none;background:none;border:0;color:var(--ink);font:600 .9rem 'DM Sans',sans-serif}.skip{position:absolute;left:1rem;top:-5rem;background:var(--coral);color:#fff;padding:.7rem 1rem;z-index:99}.skip:focus{top:.5rem}
  @media(max-width:850px){.header-inner{padding:.75rem 1.15rem}.menu-toggle{display:flex;align-items:center;gap:.65rem;min-height:44px;padding:.4rem}.menu-icon{font-size:1.4rem;color:var(--coral)}.site-header nav{display:flex;position:absolute;top:100%;left:0;right:0;padding:1rem 1.2rem 1.3rem;background:var(--paper);border-bottom:1px solid var(--line);align-items:stretch;gap:0;flex-direction:column}.site-header nav.enhanced{display:none}.site-header nav.enhanced.open{display:flex}.site-header nav a{padding:.95rem .25rem;border-bottom:1px solid var(--line)}.site-header nav .nav-contact{border-bottom:1px solid var(--coral)}}
</style>
