<script>
  // cart button
  import CartButton from "../Cart/CartButton.svelte";
  // global store
  import { link } from "svelte-routing";
  import globalStore from "../../stores/globalStore";
  let openSidebar = globalStore.toggleItem;
</script>

<nav class="navbar">
  <div class="nav-center">
    <!-- sidebar toggle -->
    <button 
      class="btn-sidebar-toggle" 
      on:click={() => {
        console.log('open sidebar');
        openSidebar('sidebar', true);
      }}>
      <i class="fas fa-bars" />
    </button>
    <!-- logo -->
    <a href="/" use:link class="nav-logo">
      <img src="/assets/images/logo.svg" class="logo" alt="razors logo" />
    </a>
    <!-- cart button -->
    <CartButton />
  </div>
</nav>
