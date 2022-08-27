<script>
  import Header from "./Components/Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import SiCalculator from "./Components/SI_Calculator.svelte";
  import CiCalculator from "./Components/CI_Calculator.svelte";
  let selected = "Simple Interest";
  const ChnageCalculator = (event) => {
    selected = event.detail.selected;
  };
</script>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css?family=Ubuntu"
    rel="stylesheet"
  />
</svelte:head>
<body>
  <Header on:selectChange={ChnageCalculator} />
  <div class="main-box">
    {#if selected == "Simple Interest"}
      <SiCalculator />
    {:else if selected === "Compound Interest"}
      <CiCalculator />
    {/if}
  </div>
  <Footer />
</body>

<style>
  body {
    font-family: "Ubuntu";
    margin: 0;
    background-color: #ccc;
  }
  .main-box {
    background-color: white;
    margin: 15px;
    border: 1px solid #fdfdfd;
    box-shadow: 0px 10px 24px rgba(0, 0, 0, 0.05),
      0px 2px 6px rgba(0, 0, 0, 0.04), 0px 0px 1px rgba(0, 0, 0, 0.04);
    border-radius: 9px;
  }
</style>
