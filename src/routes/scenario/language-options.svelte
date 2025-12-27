<script>
  export let scenario;
  import Section from "$lib/section.svelte";

  function setLanguage(language, sce) {
    sce.language = language;
    scenario = sce;
    document.getElementById("updateButton").click();
  }
</script>

<Section title={`Language & Options`} bind:isVisible={scenario.languageOptions.isVisible}>
  <!-- Overwriting Headings -->
  <label class="label mb-0" for="adversaryPreview">Translation Support Features</label>
  <!-- Languages -->
  <div class="buttons has-addons mb-0">
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "en"}
      on:click={setLanguage("en", scenario)}>English</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "de"}
      on:click={setLanguage("de", scenario)}>Deutsch</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "pl"}
      on:click={setLanguage("pl", scenario)}>Polski</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "fr"}
      on:click={setLanguage("fr", scenario)}>Français</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "zh"}
      on:click={setLanguage("zh", scenario)}>中文</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "hu"}
      on:click={setLanguage("hu", scenario)}>Magyar</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "ar"}
      on:click={setLanguage("ar", scenario)}>عربي</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "ko"}
      on:click={setLanguage("ko", scenario)}>한국인</button>
    <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "ja"}
      on:click={setLanguage("ja", scenario)}>日本語</button>
      <button
      class="button is-small is-success"
      class:is-light={scenario.language !== "es"}
      on:click={setLanguage("es", scenario)}>Español</button>
  </div>
</Section>
