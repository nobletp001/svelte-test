<script>
    let isOpen = false;

    function toggleDropdown() {
        isOpen = !isOpen;
    }

    function handleItemClick() {
        // Handle click logic for each item in the dropdown
    }
</script>

<style lang="scss">
    @import '../styles/variables.scss'; // Import your SCSS variables

    .button-all-posts {
        background: transparent;
        border: none;
        cursor: pointer;
        display: flex;
        align-items: center;
        color: $text-primary; /* Use SCSS variable for color */
        font-size: 1.5rem; /* Example font size */
        position: relative; /* Position for dropdown menu */
    }

    .dropdown-icon {
        margin-left: 0.5rem; /* Adjust as needed */
        transition: transform 0.3s ease; /* Smooth animation */
        transform: rotate(0deg); /* Initial rotation */
        fill: $text-primary; /* Use SCSS variable for icon color */
    }

    .dropdown-icon.open {
        transform: rotate(180deg); /* Rotate when open */
    }

    .dropdown-menu {
        display: none;
        position: absolute;
        top: calc(100% + 0.5rem); /* Position below button */
        left: 0;
        background-color: #fff; /* Example dropdown background color */
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Example shadow */
        z-index: 1000; /* Ensure dropdown is above other content */
        margin-top: 0.5rem; /* Adjust positioning */
        padding: 0.5rem 0;
        border-radius: 4px;
    }

    .dropdown-menu.open {
        display: block; /* Show when open */
    }

    .dropdown-item {
        padding: 0.5rem 1rem;
        cursor: pointer;
        transition: background-color 0.3s ease;

        &:hover {
            background-color: #f0f0f0; /* Example hover background color */
        }
    }
</style>

<div class="button-all-posts" on:click={toggleDropdown}>
    All Posts
    <svg class="dropdown-icon {isOpen ? 'open' : ''}" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16">
        <path d="M8 11L3 6h10z" />
    </svg>
    <div class="dropdown-menu {isOpen ? 'open' : ''}">
        <div class="dropdown-item" on:click={handleItemClick}>Post 1</div>
        <div class="dropdown-item" on:click={handleItemClick}>Post 2</div>
        <div class="dropdown-item" on:click={handleItemClick}>Post 3</div>

    </div>
</div>
