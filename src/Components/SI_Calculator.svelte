<script>
  let principle = 1000,
    rate_of_interest = 6,
    time_period = 5;

  $: total_interest = Math.round(
    (principle * rate_of_interest * time_period) / 100,
    2
  );
  $: total_amount = Number(principle) + Number(total_interest);
</script>

<div class="content">
  <div class="content-items">
    <p>Principal Amount (₹)</p>
    <input bind:value={principle} class="input-box" />
  </div>
  <div class="content-items">
    <p>Rate of interest (p.a)</p>
    <input bind:value={rate_of_interest} class="input-box" />
  </div>
  <div class="content-items">
    <p>Time Period</p>
    <input bind:value={time_period} class="input-box" />
  </div>
  <hr />
  <div class="si_output">
    <p>Principal amount : {principle}</p>
    <p>Total Interest : {total_interest}</p>
    <p>Total Amount : {total_amount}</p>
  </div>
</div>

<style>
  .content {
    padding: 15px;
  }
  .content-items {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .input-box {
    width: 35%;
    height: 30px;
    background-color: #d3f2ea;
    border: none;
    border-radius: 4px;
  }
</style>
