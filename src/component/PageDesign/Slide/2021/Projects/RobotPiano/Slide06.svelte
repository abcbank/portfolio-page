<script>
    import Page01 from "./Slide06/Page01.svelte";
    import Page02 from "./Slide06/Page02.svelte";
    import Page03 from "./Slide06/Page03.svelte";
    import Page04 from "./Slide06/Page04.svelte";
    import Page05 from "./Slide06/Page05.svelte";
    import Page06 from "./Slide06/Page06.svelte";
    import Page07 from "./Slide06/Page07.svelte";
    import Page08 from "./Slide06/Page08.svelte";
    import Page09 from "./Slide06/Page09.svelte";
    import Page10 from "./Slide06/Page10.svelte";
    import Page11 from "./Slide06/Page11.svelte";
    import Page12 from "./Slide06/Page12.svelte";
    import Page13 from "./Slide06/Page13.svelte";

    import DefaultSlide from "../../../defaultSlide.svelte";
    export let color;
    export let curPage;
    export let maxPage;

    let Pages =[
        { index: 1, component:Page01 }, 
        { index: 2, component:Page02 }, 
        { index: 3, component:Page03 }, 
        { index: 4, component:Page04 }, 
        { index: 5, component:Page05 }, 
        { index: 6, component:Page06 }, 
        { index: 7, component:Page07 }, 
        { index: 8, component:Page08 }, 
        { index: 9, component:Page09 }, 
        { index: 10, component:Page10 }, 
        { index: 11, component:Page11 }, 
        { index: 12, component:Page12 }, 
        { index: 13, component:Page13 }]
</script>

<DefaultSlide Pages={Pages} bind:curPage={curPage} bind:maxPage={maxPage} bind:color={color} />