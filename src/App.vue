<script setup>
import { onMounted, ref } from "vue";

const year = ref(null);
onMounted(() => {
  const start = 2024;
  const current = new Date().getFullYear();
  year.value.textContent = start === current ? current : `${start}–${current}`;
});
</script>

<template>
  <main>
    <div class="header">
      <div class="title">
        <img alt="avatar" src="https://img.xiaoyuan151.net/avatar.jpg" />
        <h1>XiaoYuan MC</h1>
      </div>
      <p>
        XiaoYuan MC 是一个由<a href="//www.xiaoyuan151.com">小源151</a
        >持有并运营的 Minecraft: Java Edition 服务器。
      </p>
      <p>
        对 XiaoYuan MC 感兴趣？请联系：<a href="mailto:contact@xiaoyuan151.com"
          >contact@xiaoyuan151.com</a
        >
      </p>
    </div>
  </main>
  <footer>
    <p>
      &copy; 版权所有 <span ref="year"></span> 小源151 | 保留所有权利 |
      <a href="https://icp.gov.moe/?keyword=20250319" target="_blank"
        >萌ICP备20250319号</a
      >
    </p>
    <p>
      <a href="//www.xiaoyuan151.com/privacy">隐私政策</a> |
      <a href="//www.xiaoyuan151.com/terms">使用条款</a>
    </p>
  </footer>
</template>

<style scoped>
a {
  color: inherit;
  text-decoration: none;
  user-select: none;
}

main {
  width: 100%;
  max-width: 760px;
  margin: 0 auto;
  padding: 14px 6px 38px;
}

.header {
  width: 100%;
  margin: 24px auto 12px;
  display: flex;
  flex-direction: column;
  gap: 5px;
  align-items: center;
  justify-content: center;
}

.header p {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  white-space: nowrap;
}

.header a {
  font-weight: bold;
}

.header a:hover {
  color: var(--color-border-hover);
}

.title {
  width: fit-content;
  display: flex;
  flex-direction: row;
  gap: 10px;
  align-items: center;
  justify-content: center;
  user-select: none;
}

.title img {
  height: 80px;
  border-radius: 10px;
}

footer {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

footer a {
  font-weight: bold;
}

footer a:hover {
  color: var(--color-border-hover);
}
</style>
