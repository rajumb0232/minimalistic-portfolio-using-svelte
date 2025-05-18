<script>
  export let text;
  export let isAnimated = false;
</script>

<style>
  .animated-gradient {
    background-size: 200% auto;
    animation: shimmer 3s linear infinite;
  }

  @keyframes shimmer {
    0% {
      background-position: 100% center;
    }
    50% {
      background-position: 0% center;
    }
    100% {
      background-position: -100% center;
    }
  }
</style>

<h1
  class={`text-4xl font-extrabold transition-all duration-500 
    ${isAnimated ? 'text-transparent bg-clip-text animated-gradient' : 'text-white'}`}
  style={isAnimated ? 'background-image: linear-gradient(90deg, #fff, #772fce, #0ea5e9, #000, #3CA3C2, #fff);' : ''}
>
  {text}
</h1>
