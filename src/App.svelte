<script>
  // @ts-ignore
  import Viz from "./Viz.svelte";
</script>

<main>
  <div class="header">
    <div class="info">
      <h1 class="syne-head">Weather of emotion</h1>
      <p class="syne-text">
        I've been tracking my emotions since 2021, after wrapping up my CBT
        therapy. When I first sat down with my therapist, he asked what I hoped
        to achieve, and I told him, 'I just want clear skies in my head every
        morning. But that’s like expecting perfect weather every day. It took me
        a while to realize I can’t control the sky, but I can learn to live with
        whatever weather comes my way. After 40 months of tracking this data, I
        think I'm getting better at dealing with the gloomy sky in my head. As
        you can see in the data, I could be happy with anxiety someday and mixed
        emotions.
      </p>
    </div>
    <div class="howto">
      <div class="info">
        <h2 class="syne-head">How to read</h2>
        <p class="syne-text">
          Each emoji on the chart shows the average emotional score for the
          month, with bigger sizes meaning things got intense from scale 1 to 10
        </p>
      </div>
      <div class="item">
        <div class="list">
          <img src="/sun.png" alt="sun" class="icon" />
          <div class="syne-text">Happy</div>
        </div>
        <div class="list">
          <img src="/rain.png" alt="rain" class="icon" />
          <div class="syne-text">Sad</div>
        </div>
        <div class="list">
          <img src="/cloud.png" alt="cloud" class="icon" />
          <div class="syne-text">Anxiety</div>
        </div>
        <div class="list">
          <img src="/light.png" alt="lightning" class="icon" />
          <div class="syne-text">Angry</div>
        </div>
        <div class="list">
          <img src="/fog.png" alt="fog" class="icon" />
          <div class="syne-text">Tried</div>
        </div>
        <div class="list">
          <img src="/snow.png" alt="snow" class="icon" />
          <div class="syne-text">Excited</div>
        </div>
      </div>
    </div>
  </div>
  <Viz />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Syne+Tactile&family=Syne:wght@400..800&display=swap");

  .syne-head {
    font-family: "Syne Tactile", system-ui;
    font-style: normal;
    line-height: 1;
  }

  :global(.syne-text) {
    font-family: "Syne", sans-serif;
    font-optical-sizing: auto;
    line-height: 1.5;
  }

  main {
    min-height: 100vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-image: linear-gradient(0deg, #dbffce 0%, #f8f8f8 10%, #d7f8ff 100%);
    background-attachment: fixed;
    
  }

  h1 {
    font-size: 72px;
  }

  h1,
  h2 ,
  :global(body) {
    margin: 0;
  }

  p {
    font-size: 16px;
    font-style: normal;
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 40px;
    padding-top: 24px;
    padding-bottom: 24px;
    gap: 40px;
  }

  .info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    text-align: left;
    flex: 1 0;
  }

  .howto {
    display: flex;
    padding: 24px;
    gap: 24px;
    flex: 1 0;
    background-color: #ffffff;
    border-radius: 8px;
  }

  .item {
    display: flex;
    align-items: flex-start;
    align-content: flex-start;
    gap: 16px 40px;
    flex: 1 0 0;
    flex-wrap: wrap;
  }

  .list {
    display: flex;
    width: 104px;
    height: 48px;
    align-items: center;
    gap: 16px;
  }

  .icon {
    width: 40px;
    height: 40px;
  }

  @media (max-width: 744px) {
    main {
      overflow: scroll;
      justify-content: flex-end;
    }

    h1 {
      font-size: 56px;
    }

    p {
      font-size: 14px;
    }

    .header {
      flex-direction: column;
      justify-content: center;
      align-self: stretch;
      height: fit-content;
    }

    .howto {
      flex-direction: column;
      align-self: stretch;
    }
  }
</style>
