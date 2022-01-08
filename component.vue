
<template>
<a href="#" @click.prevent="toAnchor">To Anchor</a>

<div id="anchor">
With Anchor section
</div>
</template>

<script>
import {gsap} from 'gsap';
import { ScrollToPlugin } from "gsap/ScrollToPlugin";

setup() {
gsap.registerPlugin(ScrollToPlugin);
const toAnchor = () => {
      gsap.to(window, {
        duration: 1,
        scrollTo: props.anchor,
        ease: "power2",
      });
    };
    
    return {
toAnchor
}
</script>
