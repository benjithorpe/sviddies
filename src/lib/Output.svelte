<script>
  import { temporaryHolder } from "../store.js";
</script>

<section>
  <textarea
    name=""
    id=""
    cols="30"
    rows="10"
    bind:value={$temporaryHolder}
    disabled
  />
</section>
