<script>
    import { Device, Color, season } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
</script>

<DefaultPage color={color} fontSize={subhead}>
    <p>프로젝트 한계</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            - 도착 예정 시간을 계산할때 현재 교통 상황을<br/>
            &nbsp;&nbsp;고려하지 않음
        </p>
    </div>
</DefaultPage>
<style>
</style>