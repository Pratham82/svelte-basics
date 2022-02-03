<script>
  const header = 'Svelete Basics'
  import ChildComponent from './pages/ChildComponent.svelte'
  import Couner from './pages/Counter.svelte'
  import ToggleSwitch from './pages/ToggleSwitch.svelte'
</script>

<main>
  <h1>{header}</h1>
  <!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->

  <!-- Passing props in child component -->
  <!-- <ChildComponent data={'Data from parent'} /> -->
  <!-- <Couner /> -->
  <ToggleSwitch />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    width: 60%;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 300;
    margin: 10px 0;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
