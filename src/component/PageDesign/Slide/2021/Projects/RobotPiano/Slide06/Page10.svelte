<script>
    import { Device, Color, season } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
</script>

<DefaultPage color={color} fontSize={subhead}>
    <p>강약 조절</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            {#if $Device["isSmallScreen"]}
            - 피아노는 눌리는 강약조절을 통해 멜로디에<br/>
            &nbsp;&nbsp;감정을 넣음<br/>
            - 다만 실린더를 통해 건반을 때리는 방식으론<br/>
            &nbsp;&nbsp;강약 조절을 하는 것이 불가능했음
            {:else}
            - 피아노는 눌리는 강약조절을 통해 멜로디에감정을 넣음<br/>
            - 다만 실린더를 통해 건반을 때리는 방식으론 강약 조절을 하는<br/>
            &nbsp;&nbsp;것이 불가능했음
            {/if}
        </p>
    </div>
</DefaultPage>
<style>
</style>