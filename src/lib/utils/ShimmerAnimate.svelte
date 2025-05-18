<script>
  export let text;
  export let isAnimated = false; // Trigger to true to animate
  export let delay = 0;
</script>

<span class="text-white relative inline-block">
  {text}
  {#if isAnimated}
    <span
      class="absolute inset-0 text-transparent bg-clip-text shimmer-overlay"
      style={`animation-delay: ${delay}ms;`}
    >
      {text}
    </span>
  {/if}
</span>

<style>
  .shimmer-overlay {
    background-image: linear-gradient(
      90deg,
      #ffffff 0%,
      #772fce 30%,
      #0ea5e9 60%,
      #ffffff 100%
    );
    background-size: 200% auto;
    animation: shimmer 1.5s ease-in-out forwards;
    pointer-events: none;
  }

  @keyframes shimmer {
    0% {
      opacity: 0;
      background-position: 100% center;
    }
    40% {
      opacity: 1;
    }
    100% {
      opacity: 0;
      background-position: 0% center;
    }
  }
</style>
