<script lang="ts">
  import Gallery from "./Gallery.svelte";
  import Header from "./Header.svelte";
  import Section from "./Section.svelte";
</script>

<Header />
<main>
  <Section bgColor="var(--secondary-color)">
    <img
      alt="Startup Team"
      src="https://static.wixstatic.com/media/b3528631d4da4b0ab7a0b03f94ae070c.jpg/v1/fill/w_1410,h_660,al_c,q_85,usm_0.66_1.00_0.01/Startup%20Team.webp"
    />
    <h1>Welcome to DandySoft</h1>
  </Section>
  <Gallery />
</main>

<style>
  h1 {
    color: var(--accent-color);
    font: var(--font);
    line-height: 1.25em;
    margin-bottom: 0px;
    margin-top: 40px;
  }
  img {
    width: var(--break-lg);
    object-fit: cover;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
