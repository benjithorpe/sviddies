<script>
  export let value = "";
  export let disabled = false;
  export let placeholder = "Adds 'sv' in-front of any word in a sentence";
</script>

<textarea
  name=""
  id=""
  bind:value
  {disabled}
  {placeholder}
  class="p-2 rounded min-h-[150px] min-w-full max-w-full max-h-full shadow-lg
   focus:outline-gray-300 outline-none text-slate-600 md:min-h-[200px]"
/>
