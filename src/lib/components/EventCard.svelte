<script lang="ts">
    export let logo, cornerLogo, date;
</script>

<div class="card">
    <div class="top-left-corner-logo">
        <div class="logo" style="background-image: url({cornerLogo});"></div>
        <div class="date">{date}</div>
    </div>
    <div class="crd">
        <div class="inner-card" style="background-image: url({logo});"></div>
    </div>
    <div class="bottom-right-corner-logo">
        <div class="logo" style="background-image: url({cornerLogo});"></div>
        <div class="date">{date}</div>
    </div>
</div>

<style>
    .date {
        text-align: center;
        margin-top: 0.2rem;
    }
    .top-left-corner-logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 2rem;
    }
    .bottom-right-corner-logo {
        display: flex;
        flex-direction: column;
        align-items: center;
        transform: rotate(180deg);
        flex: 1;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        width: 2rem;
    }
    .card {
        display: flex;
        background-color: black;
        width: fit-content;
        height: fit-content;
        padding: 0.5rem;
        border: 2px solid #554b87;
        border-radius: 20px;
        margin-top: 4rem;
        animation: scatter 0.8s ease-in-out forwards;
        transition: all 0.5s ease-in-out;
    }
    @keyframes scatter {
        0% {
            opacity: 0;
            transform: translate(-50%, -50%) scale(0.2) rotate(-60deg);
        }

        100% {
            opacity: 1;
        }
    }
    .crd {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 12rem;
        aspect-ratio: 2/3;
        padding: 2rem 0;
    }
    .logo {
        width: 2rem;
        height: 2rem;
        background-size: contain;
        background-position: center;
        border-radius: 100%;
    }
    .inner-card {
        background-size: contain;
        background-position: center;
        width: 100%;
        height: 100%;
        background-repeat: no-repeat;
        border-radius: 10px;
    }
</style>
