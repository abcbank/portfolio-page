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
    <p>IO</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            - 건반 누르는 용 실린더 및 서스테인 제어<br/>
            - IO 회로의 경우, 직접 만능기판으로 만들어 사용<br/>
            - 아두이노를 사용해 펌웨어 작성<br/>
        </p>
    </div>
</DefaultPage>
<style>
</style>