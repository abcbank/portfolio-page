<script>
    import { Device } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
</script>
<DefaultPage color={color} fontSize={subhead}>
    <p>Snap 연주 - 음 연주 쓰레드</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            {#if $Device["isSmallScreen"]}
            - 음 연주 쓰레드 프로세스<br/>
            &nbsp;&nbsp;1. 서스테인 처리<br/>
            &nbsp;&nbsp;2. 지정된 음에 해당되는 실린더 내림<br/>
            &nbsp;&nbsp;3. 로봇의 z 좌표를 일정 값만큼 내림<br/>
            &nbsp;&nbsp;4. 음의 길이만큼 대기<br/>
            &nbsp;&nbsp;5. 로봇의 z 좌표를 일정 값만큼 올림<br/>
            &nbsp;&nbsp;6. 지정된 음에 해당되는 실린더 올림<br/>
            &nbsp;&nbsp;7. 해당 음이 block의 마지막일 경우, 로봇 핸드의<br/>
            &nbsp;&nbsp;IO를 모두 끈 후 block의 위치로 이동
            {:else}
            - 음 연주 쓰레드 프로세스<br/>
            &nbsp;&nbsp;1. 서스테인 처리<br/>
            &nbsp;&nbsp;2. 지정된 음에 해당되는 실린더 내림<br/>
            &nbsp;&nbsp;3. 음의 길이만큼 대기<br/>
            &nbsp;&nbsp;4. 지정된 음에 해당되는 실린더 올림<br/>
            &nbsp;&nbsp;5. 해당 음이 block의 마지막일 경우, 로봇 핸드의 IO를 모두 끈 후 block의<br/>
            &nbsp;&nbsp;위치로 이동
            {/if}
        </p>
    </div>
</DefaultPage>