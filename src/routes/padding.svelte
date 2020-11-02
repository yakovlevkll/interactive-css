<h1>Padding</h1>

<p>Padding is a ....</p>

<label for="padding-top">padding-top: {padding.top}</label>
<input
type="range"
id="padding-top"
name="padding-top"
min="0"
max="20"
bind:value={padding.top}
/>

<label for="padding-left">padding-left: {padding.left}</label>
<input
type="range"
class="range"
id="padding-left"
name="padding-left"
min="0"
max="20"
bind:value={padding.left}
/>

<div class="parent" style="{parentStyle}">
    {#each [1, 2, 3, 4, 5] as el (el)}
    <div class="child"></div>
    {/each}
</div>


<script>
    const padding = {
      top: 0,
      right: 0,
      bottom: 0,
      left: 0
    }

    $: parentStyle = Object.entries(padding)
		.map(([key, val]) => `padding-${key}: ${val}px`)
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