<script>
    import { Device } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'
    import { fade } from "svelte/transition";
    import { onMount } from "svelte";

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
    let img;
    let t
	let loaded = false;
	let failed = false;
	let loading = false;
    let src = "";

</script>
<DefaultPage color={color} fontSize={subhead}>
    <div style="font-size:{context}rem;">
        <a href="https://github.com/abcbank/PiCameraServer">
            소스 코드의 경우, 깃허브 링크를 참고해주세요.
        </a>
    </div>
</DefaultPage>

<style>
    div{
        height:100%;
        width:100%; 
		flex: 1 0 auto;
	    align-items: center;
		justify-content: center;
		display: flex;
		text-align: center;
    }
    iframe{

    }
</style>