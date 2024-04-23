---
title: "Animation"
date: 2024-04-08
---

<script src="/js/wasm_go.js"></script>
<script>
    const go = new Go();
    WebAssembly.instantiateStreaming(fetch("/wasm/animation.wasm"), go.importObject).then((result) => {
        go.run(result.instance);
    });
</script>
<a class="no-colide" href="/en/demos">Back to demo screen</a>