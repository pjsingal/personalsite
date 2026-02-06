<script>
  export let segment;
</script>

<style>
  nav {
    border-top: 3px solid var(--themeColor);
    font-weight: 500;
    text-transform: uppercase;
    font-size: 0.9rem;
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    min-height: 3rem;
    /* overflow: hidden; */
    box-sizing: content-box;
    z-index: 24;
    background-color: white;
  }

  nav div.contentWrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: inline-block;
    padding: 0;
    margin: 0 0.8rem;
  }

  a::after {
    position: absolute;
    content: "";
    width: 80%;
    margin-left: 10%;
    height: 4px;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
    background-color: var(--themeColor);
    display: block;
    bottom: 0;
    transform: scaleX(0);
    transition: transform 0.3s ease;
  }

  a.selected::after {
    transform: scaleX(1);
  }

  a {
    position: relative;
    text-decoration: none;
    height: 3rem;
    display: flex;
    align-items: center;
    transition: color 0.3s ease;
    color: var(--darkGrey) !important;
  }

  picture.logo > * {
    height: 2rem;
    width: 8.33rem;
  }
</style>

<nav>
  <div class="contentWrapper">
    <div class="logo">
      <a class:selected={!segment} href=".">
        <picture class="logo">
          <source srcset="logo.webp" type="image/webp" />
          <source srcset="logo.png" type="image/png" />
          <img src="logo.png" alt="Patrick Singal" />
        </picture>
      </a>
    </div>
    <ul>
      <li>
        <a class:selected={segment === 'cv'} href="cv">
          CV
        </a>
      </li>
      <li>
        <a class:selected={segment === 'projects'} href="projects">Projects</a>
      </li>

      <li>
        <a class:selected={segment === 'qvft'} href="qvft">
          QVFT
        </a>
      </li>
      <li>
      <a href="https://www.linkedin.com/in/patricksingal" target="_blank" rel="noopener noreferrer">LinkedIn</a>
      </li>
      <li>
      <a href="https://scholar.google.com/citations?view_op=list_works&hl=fr&authuser=2&user=5EXelpYAAAAJ" target="_blank" rel="noopener noreferrer">Google Scholar</a>
      </li>
      <li>
      <a href="https://github.com/pjsingal" target="_blank" rel="noopener noreferrer">GitHub</a>
      </li>
    </ul>
  </div>
</nav>
