<script>
    import { Device, Color, season } from "../../../../../global"
    import DefaultPage from '../../defaultPage.svelte'
    import Icon from "../../../../Icon/Icon.svelte"
    import { onMount } from 'svelte'
    import { fade } from "svelte/transition"
    import { mdiCursorDefaultClick } from '@mdi/js';

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
    
    let Slide_01 = true;
    let Slide_02 = false;
    let animationStart = false;
    let visibility = true;
    let t;
    
    function startSlideChangeTimer(){
        clearTimeout(t);
        t = setTimeout(() => {
            Slide_01 = false;
            clearTimeout(t);
            t = setTimeout(() => {
                Slide_02 = true;
                startAnimationTimer();
            }, 300)
        }, 1000)
    }
    function startAnimationTimer(){
        clearTimeout(t);
        visibility = true;
        t = setTimeout(() => {
            animationStart = true;
            animationFinished();
        }, 2000)
    }
    function animationFinished(){
        clearTimeout(t);
        t = setTimeout(() => {
            restartAnimation();
        }, 2500)
    }
    function restartAnimation(){
        visibility = false;
        animationStart = false;
        clearTimeout(t);
        t = setTimeout(() => {
            startAnimationTimer();
        }, 1500)
    }
    onMount(() => {
        Slide_01= true;
        Slide_02 = false;
        startSlideChangeTimer();
    })
</script>

<DefaultPage color={color} fontSize={head}>
    {#if Slide_01}
        <p out:fade={{duration:200,}}>Welcome to abcBank</p>
    {:else if Slide_02}
        <div class="Section" style="height:100%; width:100%; font-size:{context}rem;" in:fade={{delay:300, duration:200}}>
            <div class="header" style="height:20%;">
                드래그를 통해 슬라이드를 이동해 보세요.
            </div>
            <div class="howToMove" style="font-size:{context}rem; left: {-head / 2}rem;">
                {#if visibility}
                <div class='animation' style="left: {!animationStart ? 75 : 25}%;"  in:fade={{duration:200}} out:fade={{duration:200}}>
                    <Icon size={head.toString() + "rem"} color={$Color["foreColor"][$season]} path={mdiCursorDefaultClick} />
                </div>
                {/if}
            </div>
        </div>
    {/if}
</DefaultPage>

<style>    
    .Section{
		display: flex;
        text-align:center;
	    align-items: center;
		justify-content: center;
        flex-direction:column;
    }
    .header{
		display: flex;
        text-align:center;
	    align-items: center;
		justify-content: center;
        width:100%;
        height:15%;
    }
    .howToMove{
        position:relative;
        font-size:1rem;
        width:100%;
        height:4rem;
    }
    .animation{
        font-size:1rem;
        text-align:center;
        width:1.5rem;
        height:1.5rem;
        top:20%;
        position:relative;
        transition: all ease 2s;
    }
</style>