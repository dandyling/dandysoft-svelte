<script lang="ts">
  export let variant: "primary" | "secondary";
  export let style: string = "";
  export let onClick: () => void;
</script>

<button
  on:click={onClick}
  style="--bg-color: {variant === 'primary'
    ? 'var(--brand-color)'
    : 'white'};--color: {variant === 'primary'
    ? 'white'
    : 'var(--brand-color)'};{style}"><slot /></button
>

<style>
  button {
    background-color: var(--bg-color);
    color: var(--color);
    padding: 12px 30px;
    border-radius: 0px;
    font-size: 18px;
    margin-bottom: 0px;
    cursor: pointer;
  }
</style>
