<script>
	import Icon from '../Icon/Icon.svelte';
	import IconButton from './IconButton.svelte';
	import {mdiChevronLeft,mdiChevronRight} from "@mdi/js"
	export let leftIcon = null;
	export let onOpen;
	export let isOpen;
	export let isDropdown;
	export let leftIconColor = "currentcolor"
	export let rightIconColor = "currentcolor"
	export let textColor = "var(--text-color)"
	function empty(){}
</script>

<div class="side-item"
	style="color:{textColor};">
	<IconButton iconColor={leftIconColor} path={leftIcon ?? ''} />
	
	<slot />
	{#if isDropdown}
        <span class="icon-right">
            <Icon  color={ rightIconColor } path={ !isOpen ? mdiChevronLeft : mdiChevronRight } />
        </span>
    {/if}
</div>

<style>
	.side-item {
		font-size:max(2vw, 0.75rem);
		height: 50px;
		display: grid;
		grid-template-columns: auto 1fr auto;
		gap: 8px;
		align-items: center;
		border-radius: var(--border-radius);
		transition: background var(--speed);
		padding: 0.5rem;
		color: var(--text-color);
	}
</style>