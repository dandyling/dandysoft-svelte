<script lang="ts">
  import Section from "./Section.svelte";
</script>

<Section bgColor="var(--brand-color)">
  <img
    alt="Team 1"
    src="https://static.wixstatic.com/media/469e00d2afd84d4998eb3742185505b1.jpg/v1/fill/w_1410,h_939,fp_0.50_0.50,q_90/469e00d2afd84d4998eb3742185505b1.webp"
  />
  <img
    alt="Team 2"
    src="https://static.wixstatic.com/media/4d2ad5a6300843d1bb5952efa6729423.jpg/v1/fill/w_1410,h_938,fp_0.50_0.50,q_90/4d2ad5a6300843d1bb5952efa6729423.webp"
  />
  <img
    alt="Team 3"
    src="https://static.wixstatic.com/media/1fb4c0ae2d604ff8b2f97e0a53bda09f.jpg/v1/fill/w_1410,h_935,fp_0.50_0.50,q_90/1fb4c0ae2d604ff8b2f97e0a53bda09f.webp"
  />
</Section>

<style>
  img {
    width: var(--break-lg);
    object-fit: cover;
    margin: 5px 0;
  }
</style>
