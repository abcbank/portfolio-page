<script>
    import { Device } from "../../../../../global"
    import DefaultPage from '../../defaultPage.svelte'

    export let color = "transparent";
    export let head = 2;
    export let subhead = 1.5;
    export let context = 1;
</script>

<DefaultPage color={color}>
    <p style="font-size: {context}rem;">제 주력 분야가 웹과 디자인이 아니지만...</p>
</DefaultPage>