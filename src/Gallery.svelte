<script lang="ts">
  import Section from "./Section.svelte";
  import Button from "./Button.svelte";
  let showMore: boolean = false;

  type Image = {
    alt: string;
    src: string;
  };

  let images: Image[] = [
    {
      alt: "Team 1",
      src:
        "https://static.wixstatic.com/media/469e00d2afd84d4998eb3742185505b1.jpg/v1/fill/w_1410,h_939,fp_0.50_0.50,q_90/469e00d2afd84d4998eb3742185505b1.webp",
    },
    {
      alt: "Team 2",
      src:
        "https://static.wixstatic.com/media/4d2ad5a6300843d1bb5952efa6729423.jpg/v1/fill/w_1410,h_938,fp_0.50_0.50,q_90/4d2ad5a6300843d1bb5952efa6729423.webp",
    },
    {
      alt: "Team 3",
      src:
        "https://static.wixstatic.com/media/1fb4c0ae2d604ff8b2f97e0a53bda09f.jpg/v1/fill/w_1410,h_935,fp_0.50_0.50,q_90/1fb4c0ae2d604ff8b2f97e0a53bda09f.webp",
    },
    {
      alt: "Team 4",
      src:
        "https://static.wixstatic.com/media/d5838190cba0447aa103713c99db4229.jpg/v1/fill/w_777,h_518,fp_0.50_0.50,q_90/d5838190cba0447aa103713c99db4229.webp",
    },
    {
      alt: "Team 5",
      src:
        "https://static.wixstatic.com/media/bafadadbe810eba6c2d754437f3164ca.jpg/v1/fill/w_779,h_518,fp_0.50_0.50,q_90/bafadadbe810eba6c2d754437f3164ca.webp",
    },
    {
      alt: "Team 6",
      src:
        "https://static.wixstatic.com/media/9dc645b2ce0445109a23ddc9a4ad0efe.jpg/v1/fill/w_776,h_518,fp_0.50_0.50,q_90/9dc645b2ce0445109a23ddc9a4ad0efe.webp",
    },
  ];

  const threshold = 3;

  const onClick = () => {
    showMore = true;
  };
</script>

<Section bgColor="var(--brand-color)">
  {#each images as image, i (image.src)}
    {#if i < threshold}
      <img alt={image.alt} src={image.src} />
    {:else if showMore}
      <img alt={image.alt} src={image.src} />
    {/if}
  {/each}
  {#if !showMore}
    <Button {onClick} style="margin-top:30px" variant="primary"
      >Load More</Button
    >
  {/if}
</Section>

<style>
  img {
    width: var(--break-lg);
    object-fit: cover;
    margin: 5px 0;
  }
</style>
