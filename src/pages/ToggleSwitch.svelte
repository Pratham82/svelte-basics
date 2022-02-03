<script>
  // your script goes here
  import Header from '../components/Header.svelte'
  let status = 'loggedIn'
  const toggleLogin = () =>
    (status = status === 'loggedIn' ? 'loggedOut' : 'loggedIn')
  const stateDict = {
    loggedOut: 'Logged In',
    loggedIn: 'Logged Out',
  }
  const buttonDict = {
    loggedIn: 'Log In',
    loggedOut: 'Log Out',
  }
</script>

<!-- markup (zero or more items) goes here -->
<Header headerTitle="Toggle Switch" />
<button on:click={toggleLogin} class="btn">{buttonDict[status]}</button>
<h2>{stateDict[status]}</h2>

<style>
  /* your styles go here */
  .btn {
    border: none;
    padding: 10px 20px;
    background-color: rgb(36, 130, 252);
    color: white;
    border-radius: 5px;
    cursor: pointer;
    -webkit-box-shadow: 1px 1px 5px -2px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 1px 1px 5px -2px rgba(0, 0, 0, 0.75);
    box-shadow: 1px 1px 5px -2px rgba(0, 0, 0, 0.75);
  }
  .btn:hover {
    transition: 0.2s ease-in-out;
    background-color: rgb(0, 85, 197);
  }
  .btn:active {
    transform: scale(0.95);
    box-shadow: none;
    background-color: rgb(0, 85, 197);
  }
</style>
