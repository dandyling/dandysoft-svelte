<script lang="ts">
  type NavItem = {
    name: string;
    path: string;
  };

  let navItems: NavItem[] = [
    {
      name: "Home",
      path: "/",
    },
    {
      name: "Blog",
      path: "/blog",
    },
    {
      name: "CV",
      path: "/cv",
    },
    {
      name: "About",
      path: "/about",
    },
    {
      name: "Contact",
      path: "/contact",
    },
    {
      name: "Work",
      path: "/work",
    },
    {
      name: "Services",
      path: "/services",
    },
  ];
</script>

<header>
  <img alt="DandySoft logo" src="images/dandysoft-bw.png" />
  <nav>
    {#each navItems as n (n.path)}
      <li>
        <a href={n.path}>{n.name}</a>
      </li>
    {/each}
  </nav>
</header>

<style>
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 200px;
    background-color: var(--brand-color);
  }
  img {
    margin-top: 40px;
    width: 70px;
    height: 70px;
  }
  nav {
    margin-top: 31px;
    display: flex;
    list-style: none;
    justify-content: center;
    width: 100%;
  }
  li {
    padding: 0 10px;
  }
  a {
    color: rgb(247, 247, 247);
  }
</style>
