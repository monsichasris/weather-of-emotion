<script>
    // @ts-ignore
    import csv from "./assets/monthly_emotions.csv";

    //what it should be, but "month" | console.log(csv.map(item => item.day));
    //spread operator ...
    let months = [...new Set(csv.map((item) => Object.values(item)[0]))];

    function getEmoji(emotion) {
        if (emotion === "Happy") {
            return "/sun.png";
        } else if (emotion === "Sad") {
            return "/rain.png";
        } else if (emotion === "Anxiety") {
            return "/cloud.png";
        } else if (emotion === "Angry") {
            return "/light.png";
        } else if (emotion === "Tired") {
            return "/fog.png";
        } else if (emotion === "Excited") {
            return "/snow.png";
        }
    }

    function getScale(value) {
        return 0.4 * Math.sqrt(value);
    }

    let visible = "";

    function showTooltip(month) {
        visible = month;
    }
    function hideTooltip() {
        visible = "";
    }
</script>

<div class="timeline">
    {#each months as month}
        {@const moods = csv.filter((item) => Object.values(item)[0] === month)}
        <div
            class="mood"
            role="tooltip"
            on:mouseenter={() => showTooltip(month)}
            on:mouseleave={hideTooltip}
        >
        {#if visible === month}
            <div class="tooltip syne-text">
                <span class="bold">{month}</span>
                {#each moods as mood}
                    <div class="tooltiptext">
                        <div>{mood.emotion}:</div>
                        <div>{parseFloat(mood.value).toFixed(2)}</div>
                    </div>
                {/each}
            </div>
        {/if}
            {#each moods as mood}
                <img
                    style="transform: scale({getScale(mood.value)})"
                    alt={mood.emotion}
                    class="emoji"
                    src={getEmoji(mood.emotion)}
                />
            {/each}

            <div class="label syne-text">
                {#if month.endsWith("-1")}
                    <span>{month.slice(0, 4)}</span>
                {:else if month === "2021-4"}
                    <span class="annotation">Lock-down started 🔒</span>
                {:else if month === "2021-12"}
                    <span class="annotation">Lock-down ended 🔓</span>
                {:else if month === "2022-3"}
                    <span class="annotation">Instructor 1st time</span>
                {:else if month === "2022-8"}
                    <span class="annotation">Broke up 💔</span>
                {:else if month === "2022-10"}
                    <span class="annotation">Take hormones</span>
                {:else if month === "2022-12"}
                    <span class="annotation">Travel aboard</span>
                {:else if month === "2023-2"}
                    <span class="annotation">Start LDR 💘</span>
                {:else if month === "2023-8"}
                    <span class="annotation">Start Dancing</span>
                {:else if month === "2024-3"}
                    <span class="annotation">Got an offer from school</span>
                {/if}
            </div>
        </div>
    {/each}
</div>

<style>
    .timeline {
        display: flex;
        position: relative;
        flex-direction: row;
        overflow: scroll;
        padding-left: 40px;
        padding-right: 128px;
    }

    .mood {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .mood:hover {
        background-color: white;
        border-radius: 8px;
    }

    .emoji {
        width: 80px;
        height: 80px;
    }

    .label {
        font-size: 12;
        text-align: center;
        padding: 8px;
    }

    .bold {
        font-weight: 600;
    }

    .tooltip {
        position: absolute;
        background-color: white;
        padding: 8px;
        border-radius: 4px;
        font-size: 12px;
        height: fit-content;
        width: 80px;
        margin-left: 160px;
        z-index: 1;
    }

    .tooltiptext {
        display: flex;
        justify-content: space-between;
    }

    .annotation {
        display: flex;
        width: 100%;
        align-items: left;
        font-size: 12px;
        opacity: 75%;
    }

    ::-webkit-scrollbar {
        width: 0px;
    }
</style>
