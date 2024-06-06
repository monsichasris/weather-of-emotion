<script>

</script>


<main>
  <div class = "header">
    <div class = "info">
      <h1 class = "syne-head">Weather of emotion</h1>
      <p class = "syne-text">I've been tracking my emotions since 2021, after wrapping up my CBT therapy. When I first sat down with my therapist, he asked what I hoped to achieve, and I told him, 'I just want clear skies in my head every morning. But that’s like expecting perfect weather every day. It took me a while to realize I can’t control the sky, but I can learn to live with whatever weather comes my way.
After 40 months of tracking this data, I think I'm getting better at dealing with the gloomy sky in my head. As you can see in the data, I could be happy with anxiety someday and mixed emotions. (I'm not tracking just good or bad days because I believe it's more complicated than that.)</p>
    </div>
    <div class = "howto">
      <div class = "info">
        <h2 class="syne-head">How to read</h2>
        <p class="syne-text">Each emoji on the chart shows the average emotional score for the month, with bigger sizes meaning things got intense</p>
      </div>
      <div class = "item">
        <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/snowflake_2744-fe0f.png" alt="snow" class="icon"/>
          <div class="syne-text">Excited</div>
        </div>
         <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/sun_2600-fe0f.png" alt="sun" class="icon"/>
          <div class="syne-text">Happy</div>
        </div>
         <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/cloud_2601-fe0f.png" alt="cloud" class="icon"/>
          <div class="syne-text">Anxiety</div>
        </div>
         <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/droplet_1f4a7.png" alt="rain" class="icon"/>
          <div class="syne-text">Sad</div>
        </div>
         <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/high-voltage_26a1.png" alt="lightning" class="icon"/>
          <div class="syne-text">Angry</div>
        </div>
         <div class="list">
          <img src="https://em-content.zobj.net/source/apple/391/fog_1f32b-fe0f.png" alt="fog" class="icon"/>
          <div class="syne-text">Tried</div>
        </div>

      </div>
    </div>
  </div>

</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne&family=Syne+Tactile&display=swap');

  .syne-head {
  font-family: "Syne Tactile", system-ui;
  font-style: normal;
  line-height: 0;

  }

  .syne-text {
  font-family: "Syne", sans-serif;
  font-optical-sizing: auto;
  font-style: normal;
  line-height: 1.5;
  }

  main {
    height: 100vh;
    width: 100vw;
    top: 0; 
    left: 0; 
    position: fixed;
    overflow: hidden;
    background: linear-gradient(0deg, #DBFFCE 0%, #FFFFFF 10%, #D7F8FF 100%);

  }

  h1 {
    font-size: 72px;
  }

  p {
    font-size: 16px;
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    height: 30%;
    padding: 40px;
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
    background-color: #FFFFFF;
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

  
</style>
