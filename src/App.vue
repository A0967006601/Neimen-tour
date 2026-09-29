<script setup>
// 引入圖片資源（根據你的專案資料夾結構調整，如果放在 public 資料夾則可直接用路徑）
import templeImg from './assets/temple.jpg'
import chefImg from './assets/chef.jpg'
import mountainImg from './assets/mountain.jpg'
</script>

<template>
  <div class="tour-app">
    <!-- 1. 頂部公告條 -->
    <div class="top-banner-bar">
      <span>歡迎來到內門 USR 旅遊網！探索在地宗教文化、總舖師美食與特色農產。</span>
      <button class="close-btn">了解更多</button>
    </div>

    <!-- 2. 導覽列 -->
    <header class="navbar">
      <h1 class="logo">內門走透透 <span>NEIMEN TOUR</span></h1>
      <nav class="nav-links">
        <a href="#" class="active">首頁</a>
        <a href="#">內門景點</a>
        <a href="#">總舖師美食</a>
        <a href="#">在地文化</a>
        <a href="#">遊程快搜</a>
        <a href="#">交通指南</a>
      </nav>
      <div class="nav-right">
        <input type="text" placeholder="搜尋景點、美食..." class="search-input" />
        <button class="user-btn">會員</button>
      </div>
    </header>

    <!-- 3. 主視覺 Banner -->
    <section class="hero-section">
      <div class="hero-overlay"></div>
      <div class="hero-content">
        <span class="hero-tag">USR 地方創生專案</span>
        <h2>內門觀光與在地文化</h2>
        <p>探索宋江陣藝陣之鄉，品嚐最道地的總舖師手路菜與山城美景！</p>
        <div class="hero-btns">
          <button class="primary-btn">開始規劃行程</button>
          <button class="secondary-btn">了解在地故事</button>
        </div>
      </div>
    </section>

    <!-- 4. 特色卡片區塊 -->
    <section class="features-section">
      <h3>內門三大特色推薦</h3>
      <div class="card-grid">
        <!-- 卡片 1：特色宗教文化 -->
        <div class="card">
          <div class="card-img" :style="{ backgroundImage: `url(${templeImg})` }"></div>
          <div class="card-body">
            <h4>特色宗教文化</h4>
            <p>參訪著名的內門紫竹寺與南海紫竹寺，深入了解深厚的宋江陣藝陣文化。</p>
          </div>
        </div>

        <!-- 卡片 2：在地總舖師料理 -->
        <div class="card">
          <div class="card-img" :style="{ backgroundImage: `url(${chefImg})` }"></div>
          <div class="card-body">
            <h4>在地總舖師料理</h4>
            <p>品嚐聞名全台的內門手路菜與傳統辦桌文化，體驗道地的總舖師好手藝。</p>
          </div>
        </div>

        <!-- 卡片 3：休閒農業與自然 -->
        <div class="card">
          <div class="card-img" :style="{ backgroundImage: `url(${mountainImg})` }"></div>
          <div class="card-body">
            <h4>休閒農業與自然</h4>
            <p>漫步於內門的明媚風光，體驗龍眼、荔枝等豐富在地特產與農村樂趣。</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 5. 頁尾 -->
    <footer class="footer">
      <p>&copy; 2026 內門旅遊網 Neimen Tourism Website. All Rights Reserved. (USR大學社會責任實踐計畫)</p>
    </footer>
  </div>
</template>

<style scoped>
.tour-app {
  width: 100%;
  margin: 0;
  padding: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f9f9f9;
  overflow-x: hidden;
}

.top-banner-bar {
  background-color: #d97706;
  color: white;
  padding: 8px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9rem;
  width: 100%;
  box-sizing: border-box;
}

.close-btn {
  background: white;
  color: #d97706;
  border: none;
  padding: 4px 12px;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  background-color: white;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  position: sticky;
  top: 0;
  z-index: 100;
  width: 100%;
  box-sizing: border-box;
}

.logo {
  font-size: 1.3rem;
  color: #b45309;
  margin: 0;
}

.logo span {
  font-size: 0.75rem;
  color: #666;
  display: block;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-links a {
  text-decoration: none;
  color: #444;
  font-weight: 500;
}

.nav-links a:hover, .nav-links a.active {
  color: #d97706;
}

.nav-right {
  display: flex;
  gap: 10px;
  align-items: center;
}

.search-input {
  padding: 6px 12px;
  border: 1px solid #ddd;
  border-radius: 20px;
  outline: none;
}

.user-btn {
  background-color: #f3f4f6;
  border: 1px solid #d1d5db;
  padding: 6px 14px;
  border-radius: 20px;
  cursor: pointer;
}

.hero-section {
  position: relative;
  background-image: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1600&q=80');
  background-size: cover;
  background-position: center;
  color: white;
  padding: 100px 20px;
  text-align: center;
  width: 100%;
  box-sizing: border-box;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(217, 119, 6, 0.85), rgba(180, 83, 9, 0.9));
}

.hero-content {
  position: relative;
  max-width: 700px;
  margin: 0 auto;
  z-index: 2;
}

.hero-tag {
  background-color: rgba(255, 255, 255, 0.25);
  padding: 5px 14px;
  border-radius: 20px;
  font-size: 0.85rem;
}

.hero-section h2 {
  font-size: 2.6rem;
  margin: 20px 0 10px 0;
}

.hero-section p {
  font-size: 1.15rem;
  margin-bottom: 30px;
}

.hero-btns {
  display: flex;
  justify-content: center;
  gap: 15px;
}

.primary-btn {
  background-color: white;
  color: #b45309;
  border: none;
  padding: 10px 24px;
  border-radius: 6px;
  font-weight: bold;
  cursor: pointer;
}

.secondary-btn {
  background-color: transparent;
  color: white;
  border: 1px solid white;
  padding: 10px 24px;
  border-radius: 6px;
  font-weight: bold;
  cursor: pointer;
}

.features-section {
  padding: 60px 20px;
  text-align: center;
  background-color: white;
  width: 100%;
  box-sizing: border-box;
}

.features-section h3 {
  font-size: 1.8rem;
  margin-bottom: 40px;
  color: #1f2937;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.card {
  background: #f9fafb;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  overflow: hidden;
  text-align: left;
  display: flex;
  flex-direction: column;
}

/* 調整圖片區塊高度與填滿方式 */
.card-img {
  height: 200px;
  background-size: cover;
  background-position: center;
  width: 100%;
}

.card-body {
  padding: 20px;
}

.card h4 {
  margin: 0 0 10px 0;
  color: #111827;
}

.card p {
  margin: 0;
  color: #4b5563;
  font-size: 0.95rem;
  line-height: 1.5;
}

.footer {
  background-color: #1f2937;
  color: #9ca3af;
  text-align: center;
  padding: 30px 20px;
  font-size: 0.9rem;
  width: 100%;
  box-sizing: border-box;
}
</style>