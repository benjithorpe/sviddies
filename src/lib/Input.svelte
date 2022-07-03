<script>
  import { temporaryHolder } from "../store.js";
  let input = "";

  const convert = (sentence) => {
    let convertedWords = [];
    const splittedWords = sentence.trim().split(" ");

    splittedWords.forEach((word) => {
      if (word.length > 1) {
        word = "sv" + word;
      }
      convertedWords.push(word);
    });

    return convertedWords.join(" ");
  };

  $: $temporaryHolder = convert(input);
</script>

<section>
  <textarea
    name=""
    id=""
    cols="30"
    rows="10"
    bind:value={input}
    placeholder="Write a sentence to be converted"
  />
</section>
