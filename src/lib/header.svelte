<script>
    // No script logic needed for this example
</script>

<style lang="scss">
    @import '../styles/variables.scss';

    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: transparent;
        padding: 1.5rem 0rem;
        width: 100%;

        @media (max-width: 768px) {
            flex-direction: column;
            align-items: flex-start;
            padding: 1rem 0rem;
        }
    }

    .app-name {
        font-size: 1.5rem;
        font-weight: 800;
        color: $text-primary;

        @media (max-width: 768px) {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
    }

    .nav-container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        .nav-links {
            display: flex;
            align-items: center;
            gap: 1.5rem;

            @media (max-width: 768px) {
                flex-direction: column;
                align-items: flex-start;
                gap: 1rem;
            }

            .nav-link {
                text-decoration: none;
                color: $text-primary;
                font-size: 0.8rem;
                font-weight: 400;

                @media (max-width: 768px) {
                    font-size: 0.7rem;
                }
            }

            .preorder-button {
                background-color: $button;
                border: none;
                color: white;
                padding: 0.3rem 0.6rem;
                font-size: 0.8rem;
                cursor: pointer;
                border-radius: 1rem;
                font-weight: 400;

                @media (max-width: 768px) {
                    font-size: 0.7rem;
                    padding: 0.2rem 0.4rem;
                }
            }
        }
    }
</style>

<header class="header">
    <div class="app-name">MISFITS</div>
    <div class="nav-container">
        <nav class="nav-links">
            <a href="#press" class="nav-link">Press</a>
            <a href="#about" class="nav-link">About</a>
            <a href="#how-to-play" class="nav-link">How to Play</a>
            <a href="#review" class="nav-link">Review</a>
            <button class="preorder-button">Preorder Now</button>
        </nav>
    </div>
</header>
