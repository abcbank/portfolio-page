<script>
    import { Device } from "../../../../../../../global"
    import DefaultPage from '../../../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
</script>

<DefaultPage color={color} fontSize={subhead}>
    <p>비닐 전처리 시퀀스</p>
    <div style="font-size:{context}rem; text-align:left; margin-top:20px;">
        <p>
            {#if $Device["isSmallScreen"]}
            1. 카메라는 컨베이어의 상단에서 연속적으로<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;촬영<br/>
            2. 컨베이어를 통해 제품이 로딩<br/>
            3. 촬영된 이미지을 통해 해당 제품이 정상<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;제품인지, 불량품인지 판단<br/>
            4. 정상 제품일 경우 초록색, 불량품일 경우<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;빨간색으로 이미지 및 제품의 바운딩 박스를<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;사용자에게 보여줌<br/>
            5. 현재 ROI에 있는 모든 제품의 개수, 각 제품 별<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;정확도 등을 사용자에게 표 형태로 보여줌
            {:else}
            1. 카메라는 컨베이어의 상단에서 연속적으로 촬영<br/>
            2. 컨베이어를 통해 제품이 로딩<br/>
            3. 촬영된 이미지을 통해 해당 제품이 정상 제품인지, 불량품인지 판단<br/>
            4. 정상 제품일 경우 초록색, 불량품일 경우 빨간색으로 이미지 및<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;제품의 바운딩 박스를 사용자에게 보여줌<br/>
            5. 현재 ROI에 있는 모든 제품의 개수, 각 제품 별 정확도 등을 사용자에게<br/>
            &nbsp;&nbsp;&nbsp;&nbsp;표 형태로 보여줌
            {/if}
        </p>
    </div>
</DefaultPage>