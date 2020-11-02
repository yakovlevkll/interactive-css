<h1>Margin</h1>

<p>Margin is a ....</p>

<label for="margin-top">margin-top: {margin.top}</label>
<input
type="range"
id="margin-top"
name="margin-top"
min="0"
max="20"
bind:value={margin.top}
/>

<label for="margin-left">margin-left: {margin.left}</label>
<input
type="range"
class="range"
id="margin-left"
name="margin-left"
min="0"
max="20"
bind:value={margin.left}
/>

<div class="parent">
    {#each [1, 2, 3, 4, 5] as el (el)}
    <div class="child" style="{childStyle}"></div>
    {/each}
</div>


<script>
    const margin = {
      top: 0,
      right: 0,
      bottom: 0,
      left: 0
    }

    $: childStyle = Object.entries(margin)
		.map(([key, val]) => `margin-${key}: ${val}px`)
        .join(';');
</script>


<style>
.parent {
  width: 100%;
  height: 100px;
  background: grey;
  box-sizing: border-box;
}

.child {
  display: inline-block;
  width: 15%;
  height: 50px;
  background: aqua;
  box-sizing: border-box;
}
</style>