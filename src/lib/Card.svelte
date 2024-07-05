<script>
    export let imageSrc;
    export let text;
</script>

<div class="card">
    <img class="card-image" src={imageSrc} alt={text} />
    <div class="card-content">
        <p>{text}</p>
        <a
            class="read-more"
            href="#"
            target="_blank"
            rel="noopener noreferrer">Read More</a
        >
    </div>
</div>

<style lang="scss">
  @import '../styles/variables.scss';

    .card {
        border-radius: 8px;
        overflow: hidden;
        width: 100%;
        .card-image {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }

        .card-content {
            padding: 1rem;

            p {
                margin: 0 0 1rem 0;
                font-size: 2rem;
                color: $text-primary;
            }

            .read-more {
                text-decoration: none;
                color:$text-primary;
                font-weight: 400;
                text-decoration: underline;

            }
        }
    }
</style>
