<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  let selectedTab = "Simple Interest";
</script>

<div class="topnav">
  <a
    on:click={() => {
      selectedTab = "Simple Interest";
      dispatch("selectChange", {
        selected: selectedTab,
      });
    }}
    class="width-50"
    class:active={selectedTab === "Simple Interest"}
    href="#news">Simple Interest</a
  >
  <a
    on:click={() => {
      selectedTab = "Compound Interest";
      dispatch("selectChange", {
        selected: selectedTab,
      });
    }}
    class="width-50"
    class:active={selectedTab === "Compound Interest"}
    href="#contact">Compound Interest</a
  >
  <!-- <a
    on:click={() => {
      selectedTab = "About Us";
      dispatch("selectChange", {
        selected: selectedTab,
      });
    }}
    class:active={selectedTab === "About Us"}
    href="#about">About Us</a
  > -->
</div>

<style>
  .topnav {
    display: flex;
    justify-content: space-evenly;
    overflow: hidden;
    background-color: #333;
  }

  .topnav a {
    float: left;
    color: #f2f2f2;
    text-align: center;
    padding: 14px 18px;
    text-decoration: none;
    font-size: 17px;
  }

  .topnav a:hover {
    background-color: #ddd;
    color: black;
  }

  .topnav a.active {
    background-color: #04aa6d;
    color: white;
  }
  .width-50 {
    width: 50%;
  }
</style>
