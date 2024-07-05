<script>
    import Button from "./Button.svelte";
</script>

<div class="cards-container">
    <!-- Card 1 -->
    <div class="card-1">
        <h2>Quick Facts</h2>
        <div class="grid-container">
            <div class="grid-row">
                <div class="grid-item">
                    <h3>Important Date</h3>
                    <p>Invented February 2017</p>
                    <p>Release November 2023</p>
                </div>
                <div class="grid-item">
                    <h3>Games spec</h3>
                    <p>40 oddly shaped American beech (Fagus grandifolia) blocks. Slipcase and drawer packaging.</p>
                </div>
                <div class="grid-item">
                    <h3>Edition</h3>
                    <p>Misfits: First Edition (Standard), limited release 250 units</p>
                </div>
            </div>
            <div class="grid-row">
                <div class="grid-item">
                    <h3>Company Operations</h3>
                    <p>Designed in London, UK.</p>
                    <p>Operating in Victoria, BC, Canada. Registered as a Washington state LLC.</p>
                </div>
                <div class="grid-item">
                    <h3>Founder and Creator</h3>
                    <p>Alexander Neumann, a 29-year-old Canadian graphic designer and front-end developer.</p>
                </div>
                <div class="grid-item">
                    <h3>Stockists and Demo Copies</h3>
                    <p>Misfits: First Edition (Standard), limited release 250 units</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Card 2 -->
    <div class="card-2">
        <h2>Assets</h2>
        <div class="button-row">
            <Button isBorderWhite={true} onClick={() => console.log("Button clicked")}>Press Release</Button>
            <Button isBorderWhite={true} onClick={() => console.log("Button clicked")}>Product Images</Button>
            <Button isBorderWhite={true} onClick={() => console.log("Button clicked")}>Brand Assets</Button>
        </div>
    </div>
</div>

<style lang="scss">
    @import "../styles/variables.scss"; // Import your SCSS variables

    .cards-container {
        display: flex;
        justify-content: space-between;
        gap: 1.8rem; /* Adjust the gap between cards */
        margin-top: 3rem;
    }

    .card-1{
        min-height: 350px; /* Adjust the minimum height of cards */
        display: flex;
        flex-direction: column;
        padding: 1.5rem;
        box-sizing: border-box;
        border-radius: 1.5rem; /* Adjust border radius */
        background-color: $card1; /* Use your variable for card background color */
        width: 60%; /* Adjust card width as needed */
        margin-bottom: 1.5rem; /* Add margin between cards */
    }

    .card-2{
        min-height: 350px; /* Adjust the minimum height of cards */
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 1.5rem;
        box-sizing: border-box;
        border-radius: 1.5rem; /* Adjust border radius */
        background-color: $card2; /* Use your variable for card background color */
        width: 40%; /* Adjust card width as needed */
        margin-bottom: 1.5rem; /* Add margin between cards */
    }
    h2 {
        font-size: 2.5rem;
        color: $white;
        margin-bottom: 1rem;
    }

    .grid-container {
        display: flex;
        flex-direction: column;
        gap: 1rem; /* Adjust gap between grid rows */
    }

    .grid-row {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem; /* Adjust gap between grid items */
    }

    .grid-item {
        flex: 1;
        max-width: calc(33.3333% - 1rem); /* Adjust width of grid items */
    }

    h3 {
        font-size: 0.8rem;
        color: $white;
    }

    p {
        font-size: 0.7rem;
        color: $white;
        line-height: 1.2; /* Adjust line height for readability */
    }

    .button-row {
        display: flex;
        gap: 1rem; /* Adjust gap between buttons */
        margin-top: 1rem; /* Add margin above buttons */
    }

    @media (max-width: 768px) {
        .cards-container {
            flex-direction: column;
        }

        .card-1,
        .card-2 {
            width: 100%; /* Cards take full width on smaller screens */
        }

        .grid-item {
            max-width: 100%; /* Grid items take full width on smaller screens */
        }
    }
</style>
