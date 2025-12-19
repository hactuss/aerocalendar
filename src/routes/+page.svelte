<script>
  const date = new Date();
  let day = date.getDate();
  let month = date.getMonth() + 1;
  let year = date.getFullYear();

  let chrday = 24,
    chrmonth = 12;
  function dayfunc(d) {
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
  <div id="Datebox" class="flex">
    <h3 id="fulldate">
      {date.getDate() + "." + month + "." + date.getFullYear()}
    </h3>

    <div id="weekday" class="flex">
      <h2>{dayfunc(date)}</h2>
    </div>
  </div>
  <div id="Datebox">
    <h3>Time until Christmas</h3>
    <h2 class="flex">
      {chrmonth - month} months, {chrday - day} days
    </h2>
  </div>
  <div id="Datebox">
    <h3>Time until {year + 1}</h3>
    <h2 class="flex">
      {12 - month} months
    </h2>
  </div>
  <!-- --
  <div id="Datebox" class="flex col">
    <div>
      <p>Time until {year + 1}</p>
      <h2>
        {12 - month} months, {month.toFixed() - day} days,
      </h2>
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
    border: solid 1px white;

    border-radius: 10px;
    backdrop-filter: blur(20px);

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
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
  .row {
    flex-direction: row;
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
