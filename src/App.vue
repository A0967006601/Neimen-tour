<script setup>
import { ref } from 'vue'

const activeTab = ref('首頁')
const handleNav = (tabName) => {
  activeTab.value = tabName
}
</script>

<template>
  <div class="neimen-container">
    <!-- 導覽列 Navbar -->
    <header class="navbar">
      <div class="logo">內門 USR 觀光導覽</div>
      <nav class="nav-links">
        <a href="#" :class="{ active: activeTab === '首頁' }" @click="handleNav('首頁')">首頁</a>
        <a href="#" :class="{ active: activeTab === '文化' }" @click="handleNav('文化')">陣頭文化</a>
        <a href="#" :class="{ active: activeTab === '美食' }" @click="handleNav('美食')">總鋪師美食</a>
        <a href="#" :class="{ active: activeTab === '景點' }" @click="handleNav('景點')">在地景點</a>
      </nav>
    </header>

    <!-- 首頁 Hero Banner 區塊 -->
    <section class="hero">
      <div class="hero-content">
        <h1>探索內門，體驗最道地的台灣人情味</h1>
        <p>結合大學社會責任（USR）推動，帶領您深入了解內門的宋江陣魅力與傳奇總鋪師文化。</p>
        <button class="cta-btn" @click="alert('歡迎來到內門觀光網！')">開始探索</button>
      </div>
    </section>

    <!-- 特色亮點區塊 Features -->
    <section class="features">
      <h2>內門三大核心魅力</h2>
      <div class="feature-grid">
        <div class="feature-card">
          <h3>陣頭之鄉</h3>
          <p>揚名國際的內門宋江陣與藝陣文化，展現台灣民間信仰與武術的力與美。</p>
        </div>
        <div class="feature-card">
          <h3>總鋪師辦桌</h3>
          <p>台灣總鋪師的發源地，道地的手路菜與辦桌文化，滿足每一位老饕的味蕾。</p>
        </div>
        <div class="feature-card">
          <h3>自然與信仰</h3>
          <p>造訪內門紫竹寺與南海紫竹寺，感受清幽的自然山林與深厚的宗教歷史。</p>
        </div>
      </div>
    </section>

    <!-- 頁尾 Footer -->
    <footer class="footer">
      <p>&copy; 2026 USR Kaohsiung Neimen Tourism Project. All Rights Reserved.</p>
    </footer>
  </div>
</template>

<style scoped>
/* 頁面整體設定，取消預設邊距並讓背景鋪滿 */
.neimen-container {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: #333;
  background-color: #f9f9f9;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  width: 100%;
  margin: 0;
}

/* 導覽列滿版設定 */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.2rem 5%;
  background-color: #2c3e50;
  color: white;
  width: 100%;
  box-sizing: border-box;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  letter-spacing: 1px;
}

.nav-links a {
  color: #bdc3c7;
  text-decoration: none;
  margin-left: 2rem;
  font-size: 1rem;
  transition: color 0.3s;
}

.nav-links a:hover, .nav-links a.active {
  color: #ffffff;
  font-weight: bold;
}

/* Hero Banner 滿版設定 */
.hero {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), 
              url('https://images.unsplash.com/photo-1508873696983-2df5c92091c7?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
  color: white;
  text-align: center;
  padding: 6rem 2rem;
  width: 100%;
  box-sizing: border-box;
}

.hero-content h1 {
  font-size: 2.8rem;
  margin-bottom: 1rem;
}

.hero-content p {
  font-size: 1.2rem;
  max-width: 600px;
  margin: 0 auto 2rem auto;
  color: #e0e0e0;
}

.cta-btn {
  background-color: #e67e22;
  color: white;
  border: none;
  padding: 0.8rem 2rem;
  font-size: 1.1rem;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.cta-btn:hover {
  background-color: #d35400;
}

/* 特色區塊滿版設定 */
.features {
  padding: 4rem 5%;
  text-align: center;
  width: 100%;
  box-sizing: border-box;
}

.features h2 {
  font-size: 2rem;
  margin-bottom: 2.5rem;
  color: #2c3e50;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.feature-card {
  background: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  transition: transform 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-card h3 {
  color: #e67e22;
  margin-bottom: 1rem;
}

.feature-card p {
  color: #666;
  line-height: 1.6;
}

/* 頁尾滿版設定 */
.footer {
  text-align: center;
  padding: 1.5rem;
  background-color: #1a252f;
  color: #888;
  margin-top: auto;
  width: 100%;
  box-sizing: border-box;
  font-size: 0.9rem;
}
</style>
