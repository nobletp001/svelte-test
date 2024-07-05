<script>
  import Header from "../lib/Header.svelte";
  import Textcontent from "../lib/Textcontent.svelte";
  import Textheader from "../lib/Textheader.svelte";
  import Card from "../lib/Card.svelte";
  import AllPostButton from "../lib/AllPostButton.svelte";
  import Button from "../lib/Button.svelte";
    import Content from "../lib/Content.svelte";

  const cards = [
    {
      imageSrc: "/image1.jpg",
      text: "Misfits Pre-sale Starts!",
    },
    {
      imageSrc: "/image2.jpg",
      text: "Misfits Featured by Yogscast Live",
    },
    {
      imageSrc: "/image3.jpg",
      text: "Read More Come see us in the UK and at Essen Spiel 2023",
    },
    // Add more card data as needed
  ];
</script>

<div class="container">
  <div class="box">
    <Header />
    <Textheader />
    <Textcontent />
    <Content/>
    <section class="session">
      <div class="button-box">
        <AllPostButton />
      </div>
      <div class="cards-container">
        {#each cards as card}
          <div class="card">
            <Card imageSrc={card.imageSrc} text={card.text} />
          </div>
        {/each}
      </div>
    </section>

    <section class="session">
      <div class="button-box">
        <AllPostButton />
      </div>
      <div class="group-button">
        <Button isActive={true} onClick={() => console.log("Button clicked")}>
          All
        </Button>
        <Button isActive={false} onClick={() => console.log("Button clicked")}>
          Misfits: Second Edition
        </Button>
        <Button isActive={false} onClick={() => console.log("Button clicked")}>
          Misfits: First Edition
        </Button>
      </div>
      <div class="cards-container">
        {#each cards as card}
          <div class="card">
            <Card imageSrc={card.imageSrc} text={card.text} />
          </div>
        {/each}
      </div>
    </section>
  </div>
</div>

<style lang="scss">
  @import "../styles/variables.scss";

  .container {
    background: $primary-color;
    min-height: 100vh;
    width: 100%;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .box {
    padding: 0 3rem;
    width: 100%;
  }

  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Three columns */
    gap: 1rem; /* Gap between cards */
  }

  .card {
    height: auto; /* Adjust height as needed */
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Example shadow */
    transition: transform 0.3s ease;

    &:hover {
      transform: translateY(-5px); /* Example hover effect */
    }
  }

  .session {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    margin-top: 3rem;
  }

  .button-box {
    display: flex;
    justify-content: flex-end;
  }

  .group-button {
    display: flex;
    gap: 0.5rem;
    align-items: center;
    justify-content: flex-end;
  }

  @media (max-width: 992px) {
    .cards-container {
      grid-template-columns: repeat(2, 1fr); /* Two columns on smaller screens */
    }
  }

  @media (max-width: 576px) {
    .cards-container {
      grid-template-columns: 1fr; /* One column on mobile screens */
    }
  }
</style>
