<script>
  const date = new Date();
  let month = date.getMonth() + 1;
  let map = new Map();
  map.set(1, "jeöö");
  console.log(map.entries());
  console.log(map.get(1));
  function day(d) {
    switch (d.getDay()) {
      case 1:
        return "Monday";
        break;
      case 2:
        return "Tuesday";
        break;
      case 3:
        return "Wednesday";
        break;
      case 4:
        return "Thursday";
        break;
      case 5:
        return "Friday";
        break;
      case 6:
        return "Saturday";
        break;
      case 7:
        return "Sunday";
        break;
    }
  }
</script>

<main>
  <h1>Aero Calendar</h1>
  <p>Hactuss</p>
  <br />
  <div id="Datebox" class="flex col">
    <h3 id="fulldate">
      {date.getDate() + "." + month + "." + date.getFullYear()}
    </h3>

    <div id="weekday" class="flex">
      <h2>{day(date)}</h2>
    </div>
  </div>
  <!---
  <div class="flex bor w">
    <h3 id="fulldate">
      {date.getDay() + "." + date.getMonth() + "." + date.getFullYear()}
    </h3>
    <div class="flex col bor w">
      {#each map as i, map}
        <div class="bor w">
          <h2>{map + 1} {day(date)}</h2>
          <h2>{i}</h2>
        </div>
      {:else}
        <p>error</p>
      {/each}
    </div>
    </div>-->
</main>

<style lang="scss">
  main {
    height: 100%;
    margin-left: 10%;
    margin-right: 10%;
  }
  #Datebox {
    margin-bottom: 1%;
    border: solid 1px black;

    border-radius: 10px;
    backdrop-filter: blur(20px);
  }
  #weekday {
    width: 100%;
    height: 100%;
  }
  .flex {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .col {
    flex-direction: column;
  }
  .bor {
    border: solid 1px black;
    margin: 1px;
  }
  .w {
    width: 100%;
  }
  /* * {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    }*/
</style>
