<script>
import GridWrapper from './gridwrapper.svelte';
import { GameState } from '../lib/stores/GameState.js';
import RotateGrid from './rotategrid.svelte';
import SwitchButton from './switchbutton.svelte';
</script>
<style>
.ControlPanel{
    display: flex;
    max-width: 30%;
    margin: 0 auto;
    align-items: center;
}
</style>
<h1 class="Current-Player">{$GameState.current_player}</h1>
<h3 class="Turn">Turn: {$GameState.turn}</h3>

<GridWrapper/>
<div class="ControlPanel">
    <RotateGrid/>
    <SwitchButton/>
</div>
