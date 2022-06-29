<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=League+Spartan:wght@300;400;500;700&display=swap" rel="stylesheet">
</svelte:head>

<script>
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
</script>

<Router {routes} />