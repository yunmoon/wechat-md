<template>
  <div id="app">
    <codemirror-editor />
    <div class="footer">
      <p>
        <span id="busuanzi_container_site_pv" style="display: inline"
          >本站总访问数：<span id="busuanzi_value_site_pv"></span></span
        ><span
          id="busuanzi_container_site_uv"
          style="padding-left: 6px; display: inline"
          >访客数：<span id="busuanzi_value_site_uv"></span
        ></span>
      </p>
      <p>
        <a target="_blank" rel="noopener" href="https://beian.miit.gov.cn/"
          ><span style="padding-right: 6px"> 蜀ICP备2023029096号-1</span></a
        ><a target="_blank" rel="noopener" href="https://beian.mps.gov.cn/"
          ><span style="padding-right: 6px">
            川公网安备51019002005981号
          </span></a
        >
      </p>
    </div>
  </div>
</template>

<script>
import CodemirrorEditor from "@/views/CodemirrorEditor.vue";

export default {
  components: { CodemirrorEditor },
  mounted() {
    console.log(1);
  },
};
</script>

<style lang="less">
// 仿 uniapp 外层全屏
html,
body,
#app {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

::-webkit-scrollbar {
  width: 6px;
  height: 6px;
  background-color: #ffffff;
}

::-webkit-scrollbar-track {
  border-radius: 6px;
  background-color: rgba(200, 200, 200, 0.3);
}

::-webkit-scrollbar-thumb {
  border-radius: 6px;
  background-color: rgba(144, 146, 152, 0.5);
}

/* CSS-hints */
.CodeMirror-hints {
  position: absolute;
  z-index: 10;
  overflow-y: auto;
  margin: 0;
  padding: 2px;
  border-radius: 4px;
  max-height: 20em;
  min-width: 200px;
  font-size: 12px;
  font-family: monospace;

  color: #333333;
  background-color: #ffffff;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.12), 0 2px 4px 0 rgba(0, 0, 0, 0.08);
}

.CodeMirror-hint {
  margin-top: 10px;
  padding: 4px 6px;
  border-radius: 2px;
  white-space: pre;
  color: #000000;
  cursor: pointer;

  &:first-of-type {
    margin-top: 0;
  }
  &:hover {
    background: #f0f0f0;
  }
}
.footer {
  width: 100%;
  margin: 0 auto;
  padding-bottom: 30px;
  p {
    margin: 0;
    text-align: center;
    font-size: 14px;
    font-weight: 100;
    color: #aaa;
    a {
      color: #aaa;
    }
  }
}
</style>
