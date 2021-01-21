<script lang="ts">
  export let bgColor: string;
</script>

<section style="--bg-color: {bgColor}"><slot /></section>

<style>
  section {
    background-color: var(--bg-color);
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 120px 0;
  }
</style>
