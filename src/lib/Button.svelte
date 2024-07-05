<script>
    // Props
    export let isActive = false;
    export let onClick = () => {};
    export let isBorderWhite = false; // New prop to control white border and text

    // Function to handle click event
    function handleClick() {
        onClick();
    }
</script>

<style lang="scss">
    @import '../styles/variables.scss'; // Import your SCSS variables

    .button {
        padding: 0.5rem 0.8rem;
        background-color: transparent;
        color: $text-primary; /* Default text color */
        border: 1px solid $text-primary; /* Default border color */
        border-radius: 1rem;
        cursor: pointer;

        @media (max-width: 768px) {
            font-size: 0.7rem; /* Reduced font size for mobile */
            padding: 0.4rem 0.6rem; /* Adjusted padding for mobile */
        }

        &.isBorderWhite {
            background-color: transparent;
            color: #fff;
            border-color: #fff;
        }
        &.active {
            background-color: $text-primary; /* Active background color */
            color: #fff; /* Active text color */
        }
    }
</style>

<button class="button {isBorderWhite ? 'isBorderWhite' : ''}" class:active={isActive} on:click={handleClick}>
    <slot></slot>
</button>
