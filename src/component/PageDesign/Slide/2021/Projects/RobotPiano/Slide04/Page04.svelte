<script>
    import { Device, Color, season } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;

    let CurPage = "main"
</script>

<DefaultPage color={color} fontSize={subhead}>
    <p>Bass Arm</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            - 사내 로봇팔 재고 사용<br/>
            - 낮은음자리의 음표들 연주를 담당<br/>
            - 이더넷을 통해 PC와 통신<br/>
            - PC의 동작에 따라 위치 이동<br/>
            - 사용 모델: P6556 (Denso)
        </p>
    </div>
</DefaultPage>
<style>
</style>