<script>
  import Textarea from "./lib/Textarea.svelte";

  const convert = (sentence) => {
    let convertedWords = [];
    const splittedWords = sentence.trim().split(" ");

    splittedWords.forEach((word) => {
      if (word.length > 1 && word.slice(0, 2) !== "sv") {
        word = "sv" + word;
      }
      convertedWords.push(word);
    });

    return convertedWords.join(" ");
  };

  let input = "";
  $: converted = convert(input);
</script>

<main class="bg-slate-200">
  <div
    class="h-screen max-w-4xl mx-auto flex flex-col md:flex-row items-center justify-center px-5 gap-5"
  >
    <!-- output textarea -->
    <section class="w-full">
      <Textarea disabled={true} placeholder="" value={converted} />
    </section>
    <!-- input textarea -->
    <section class="w-full">
      <Textarea bind:value={input} />
    </section>
  </div>
</main>
