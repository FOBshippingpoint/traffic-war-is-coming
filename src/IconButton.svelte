<script>
  export let link = "#";
  export let title = null;
  export let icon = ""; // class
</script>

<a {title} href={link} target="_blank">
  <i class={icon} />
</a>

<style>
  a {
    text-decoration: none;
    color: inherit;
  }
</style>
