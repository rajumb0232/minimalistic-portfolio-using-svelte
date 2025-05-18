<script>
  export let title;
  export let description;
  export let imageUrl;
  export let url;
</script>

<a
  href={url}
  target="_blank"
  rel="noopener noreferrer"
  class="cursor-pointer group block w-full rounded-2xl overflow-hidden bg-inherit shadow transition-all duration-300 transform hover:-translate-y-1.5 hover:shadow-2xl border border-white/70"
>
  <img
    src={imageUrl}
    alt={title}
    class="w-full h-50 object-cover transition-transform duration-300 group-hover:scale-105 filter grayscale group-hover:grayscale-0"
  />
  <div class="p-4">
    <p class="mt-2 text-sm text-gray-600 line-clamp-2">{description}</p>
    <div class="mt-4 text-right">
      <span
        class="inline-block text-blue-600 text-sm font-medium group-hover:underline"
      >
        Read More →
      </span>
    </div>
  </div>
</a>
