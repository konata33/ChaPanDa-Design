<template>
  <div id="app">
    <!-- Top Navigation -->
    <nav class="top-nav">
      <div class="nav-container">
        <!-- Logo -->
        <div class="logo">
          <img src="/cha-icon.png" alt="茶百道" class="logo-icon">
        </div>
        
        <!-- Navigation Menu -->
        <div class="nav-menu">
          <a href="#hero" class="nav-link" :class="{ active: activeSection === 'hero' }" @click="handleNavClick">首页</a>
          <a href="#products" class="nav-link" :class="{ active: activeSection === 'products' }" @click="handleNavClick">产品</a>
          <a href="#stores" class="nav-link" :class="{ active: activeSection === 'stores' }" @click="handleNavClick">门店</a>
          <a href="#about" class="nav-link" :class="{ active: activeSection === 'about' }" @click="handleNavClick">关于我们</a>
          <button class="cta-button" @click="scrollToSection('products')">立即体验</button>
        </div>
      </div>
    </nav>
    
    <!-- Main Content Area -->
    <main class="main-content">
      <div id="hero" class="hero-section">
        <div class="hero-content">
          <div class="hero-tags">
            <span class="tag">传统工艺</span>
            <span class="tag-separator">·</span>
            <span class="tag">创新茶饮</span>
            <span class="tag-separator">·</span>
            <span class="tag">品质生活</span>
          </div>
          
          <h1 class="hero-title">
            <div class="title-line-1">优质茶饮体验</div>
            <div class="title-line-2">尽在茶百道</div>
          </h1>
          
          <p class="hero-description">
            传承千年茶文化精髓，融合现代工艺创新<br>
            为您带来每一杯都值得品味的优质茶饮体验
          </p>
          
          <button class="hero-cta" @click="scrollToSection('products')">
            <span>立即探索</span>
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
              <path d="M6 12L10 8L6 4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </button>
          
          <div class="hero-subtitle">
            <span class="trust-text">已服务</span>
            <span class="highlight-number">1000+</span>
            <span class="trust-text">家门店，遍布全国各大城市</span>
          </div>
        </div>
        <div class="hero-overlay"></div>
      </div>

      <!-- Products Section -->
      <section id="products" class="products-section">
        <div class="container">
          <div class="section-header">
            <h2 class="section-title">精品茶饮系列</h2>
            <p class="section-subtitle">每一款都是匠心之作，传承与创新的完美结合</p>
          </div>
          
          <div class="products-showcase">
            <div class="products-slider">
              <!-- Product 1 -->
              <div class="product-slide">
                <div class="product-feature">
                  <div class="product-image-container">
                    <img src="/cha-product-1.png" alt="芋圆奶茶" class="product-image">
                  </div>
                  <div class="product-content">
                    <div class="product-category">招牌系列</div>
                    <h3 class="product-title">芋圆奶茶</h3>
                    <div class="product-quote">
                        <blockquote>
                         "臻选广西荔浦芋头精心调制，高含量芋头带来天然芋泥颗粒感，每一口都是沙糯香甜的极致体验。浓郁芋香在舌尖绽放，这不仅是一杯奶茶，更是对传统美味的匠心传承。"
                        </blockquote>
                    </div>
                    <div class="product-details">
                        <div class="detail-item">
                         <span class="detail-label">甄选原料：</span>
                         <span class="detail-value">广西荔浦芋头</span>
                        </div>
                        <div class="detail-item">
                         <span class="detail-label">工艺特色：</span>
                         <span class="detail-value">高芋头含量制作</span>
                        </div>
                        <div class="detail-item">
                         <span class="detail-label">口感特色：</span>
                         <span class="detail-value">沙糯香甜 · 浓郁芋香</span>
                        </div>
                    </div>
                    <div class="brand-mark">
                      <span class="brand-logo">茶百道</span>
                      <span class="brand-desc">招牌系列，经典必点</span>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Product 2 -->
              <div class="product-slide">
                <div class="product-feature reverse">
                  <div class="product-image-container">
                    <img src="/cha-product-2.png" alt="菠萝西瓜茶" class="product-image">
                  </div>
                  <div class="product-content">
                    <div class="product-category">鲜果系列</div>
                    <h3 class="product-title">菠萝西瓜茶</h3>
                    <div class="product-quote">
                      <blockquote>
                        "精选新鲜菠萝与清甜西瓜，搭配清香绿茶底，热带风情与夏日清甜的完美结合。每一块水果都新鲜饱满，每一口都是夏日的清新与甜蜜。"
                      </blockquote>
                    </div>
                    <div class="product-details">
                      <div class="detail-item">
                        <span class="detail-label">水果：</span>
                        <span class="detail-value">新鲜菠萝 + 清甜西瓜</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">茶底：</span>
                        <span class="detail-value">清香绿茶</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">特色：</span>
                        <span class="detail-value">热带清甜 · 果肉饱满</span>
                      </div>
                    </div>
                    <div class="brand-mark">
                      <span class="brand-logo">茶百道</span>
                      <span class="brand-desc">鲜果系列，健康天然</span>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Product 3 -->
              <div class="product-slide">
                <div class="product-feature">
                  <div class="product-image-container">
                    <img src="/cha-product-3.png" alt="精品咖啡系列" class="product-image">
                  </div>
                  <div class="product-content">
                    <div class="product-category">特调系列</div>
                    <h3 class="product-title">豆乳玉麒麟</h3>
                    <div class="product-quote">
                      <blockquote>
                        "独特的玉麒麟茶底搭配超厚芝士奶盖，特磨黄豆粉点缀其上。厚厚的咸香豆乳芝士口感细腻软绵，可分层品尝：先舀食奶盖的浓郁，再品茶底的清香，浓浓咸豆奶香在舌尖溢散，层次丰富的味觉盛宴。"
                      </blockquote>
                    </div>
                    <div class="product-details">
                      <div class="detail-item">
                        <span class="detail-label">茶底：</span>
                        <span class="detail-value">玉麒麟茶底</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">配料：</span>
                        <span class="detail-value">超厚芝士 + 特磨黄豆粉</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">特色：</span>
                        <span class="detail-value">分层品尝 · 咸香豆乳</span>
                      </div>
                    </div>
                    <div class="brand-mark">
                      <span class="brand-logo">茶百道</span>
                      <span class="brand-desc">特调系列，创意口感</span>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Product 4 -->
              <div class="product-slide">
                <div class="product-feature reverse">
                  <div class="product-image-container">
                    <img src="/cha-product-4.png" alt="创意特调系列" class="product-image">
                  </div>
                  <div class="product-content">
                    <div class="product-category">创意系列</div>
                    <h3 class="product-title">抹茶白桃乌龙</h3>
                    <div class="product-quote">
                      <blockquote>
                        "创新融合日式抹茶与台湾高山乌龙，加入时令白桃果肉，层次丰富的口感体验。清淡的茶香、浓郁的抹茶味与甜美的桃香完美融合。"
                      </blockquote>
                    </div>
                    <div class="product-details">
                      <div class="detail-item">
                        <span class="detail-label">茶底：</span>
                        <span class="detail-value">台湾高山乌龙</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">特调：</span>
                        <span class="detail-value">日式抹茶 + 白桃</span>
                      </div>
                      <div class="detail-item">
                        <span class="detail-label">特色：</span>
                        <span class="detail-value">层次丰富 · 创新口感</span>
                      </div>
                    </div>
                    <div class="brand-mark">
                      <span class="brand-logo">茶百道</span>
                      <span class="brand-desc">创意系列，限时特供</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="products-navigation">
            <div class="nav-counter">1/4</div>
            <div class="nav-dots">
              <span class="nav-dot active" data-slide="0"></span>
              <span class="nav-dot" data-slide="1"></span>
              <span class="nav-dot" data-slide="2"></span>
              <span class="nav-dot" data-slide="3"></span>
            </div>
            <div class="nav-buttons">
              <button class="nav-btn prev-btn">
                <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                  <path d="M12 16L6 10L12 4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </button>
              <button class="nav-btn next-btn">
                <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                  <path d="M8 4L14 10L8 16" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </button>
            </div>
          </div>
        </div>
      </section>

      <!-- Store Locations Section -->
      <section id="stores" class="stores-section">
        <div class="container">
          <div class="section-header">
            <h2 class="section-title">全国门店分布</h2>
            <p class="section-subtitle">遍布各大城市核心商圈，为您提供便捷优质的茶饮服务</p>
          </div>
          
          <div class="stores-main-content">
            <div class="stores-left">
              <div class="stores-showcase">
                <div class="stores-slider">
                  <!-- Store 1 -->
                  <div class="store-slide">
                    <div class="store-feature">
                      <div class="store-image-container">
                        <img src="/cha-shop-1.png" alt="上海静安店" class="store-image">
                        <div class="store-overlay">
                          <div class="store-status">
                            <span class="status-badge">营业中</span>
                          </div>
                        </div>
                      </div>
                      <div class="store-content">
                        <div class="store-location">
                          <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                            <path d="M10 2C7.24 2 5 4.24 5 7c0 4.5 5 9 5 9s5-4.5 5-9c0-2.76-2.24-5-5-5z" fill="#3b82f6"/>
                            <circle cx="10" cy="7" r="2" fill="white"/>
                          </svg>
                          <span class="city-name">上海 · 静安区</span>
                        </div>
                        <h3 class="store-title">静安大悦城旗舰店</h3>
                        <div class="store-address">
                          <p>静安大悦城L1层</p>
                        </div>
                        <div class="store-features">
                          <div class="feature-tag">24H营业</div>
                          <div class="feature-tag">外卖配送</div>
                        </div>
                        <div class="store-details">
                          <div class="detail-row">
                            <span class="detail-label">电话：</span>
                            <span class="detail-value">021-6666-8888</span>
                          </div>
                        </div>
                        <div class="store-actions">
                          <button class="action-btn primary">导航到店</button>
                          <button class="action-btn secondary">在线点餐</button>
                        </div>
                      </div>
                    </div>
                  </div>

                  <!-- Store 2 -->
                  <div class="store-slide">
                    <div class="store-feature reverse">
                      <div class="store-image-container">
                        <img src="/cha-shop-2.png" alt="北京朝阳店" class="store-image">
                        <div class="store-overlay">
                          <div class="store-status">
                            <span class="status-badge">营业中</span>
                          </div>
                        </div>
                      </div>
                      <div class="store-content">
                        <div class="store-location">
                          <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                            <path d="M10 2C7.24 2 5 4.24 5 7c0 4.5 5 9 5 9s5-4.5 5-9c0-2.76-2.24-5-5-5z" fill="#3b82f6"/>
                            <circle cx="10" cy="7" r="2" fill="white"/>
                          </svg>
                          <span class="city-name">北京 · 朝阳区</span>
                        </div>
                        <h3 class="store-title">三里屯太古里店</h3>
                        <div class="store-address">
                          <p>三里屯太古里南区</p>
                        </div>
                        <div class="store-features">
                          <div class="feature-tag">网红店</div>
                          <div class="feature-tag">外卖配送</div>
                        </div>
                        <div class="store-details">
                          <div class="detail-row">
                            <span class="detail-label">电话：</span>
                            <span class="detail-value">010-8888-6666</span>
                          </div>
                        </div>
                        <div class="store-actions">
                          <button class="action-btn primary">导航到店</button>
                          <button class="action-btn secondary">在线点餐</button>
                        </div>
                      </div>
                    </div>
                  </div>

                  <!-- Store 3 -->
                  <div class="store-slide">
                    <div class="store-feature">
                      <div class="store-image-container">
                        <img src="/cha-shop-3.png" alt="深圳南山店" class="store-image">
                        <div class="store-overlay">
                          <div class="store-status">
                            <span class="status-badge">营业中</span>
                          </div>
                        </div>
                      </div>
                      <div class="store-content">
                        <div class="store-location">
                          <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                            <path d="M10 2C7.24 2 5 4.24 5 7c0 4.5 5 9 5 9s5-4.5 5-9c0-2.76-2.24-5-5-5z" fill="#3b82f6"/>
                            <circle cx="10" cy="7" r="2" fill="white"/>
                          </svg>
                          <span class="city-name">深圳 · 南山区</span>
                        </div>
                        <h3 class="store-title">海岸城购物中心店</h3>
                        <div class="store-address">
                          <p>海岸城购物中心1楼</p>
                        </div>
                        <div class="store-features">
                          <div class="feature-tag">新店</div>
                          <div class="feature-tag">外卖配送</div>
                        </div>
                        <div class="store-details">
                          <div class="detail-row">
                            <span class="detail-label">电话：</span>
                            <span class="detail-value">0755-8888-9999</span>
                          </div>
                        </div>
                        <div class="store-actions">
                          <button class="action-btn primary">导航到店</button>
                          <button class="action-btn secondary">在线点餐</button>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              
              <div class="stores-navigation">
                <div class="nav-counter">1/3</div>
                <div class="nav-dots">
                  <span class="nav-dot active" data-slide="0"></span>
                  <span class="nav-dot" data-slide="1"></span>
                  <span class="nav-dot" data-slide="2"></span>
                </div>
                <div class="nav-buttons">
                  <button class="nav-btn store-prev-btn">
                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                      <path d="M12 16L6 10L12 4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                  </button>
                  <button class="nav-btn store-next-btn">
                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                      <path d="M8 4L14 10L8 16" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                  </button>
                </div>
              </div>
            </div>

            <div class="stores-right">
              <div class="stores-summary">

                <div class="summary-stats">
                  <div class="stat-item">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">门店</div>
                  </div>
                  <div class="stat-item">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">城市</div>
                  </div>
                  <div class="stat-item">
                    <div class="stat-number">24H</div>
                    <div class="stat-label">服务</div>
                  </div>
                </div>

              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- About Us Section -->
      <section id="about" class="about-section">
        <div class="container">
          <div class="section-header">
            <h2 class="section-title">关于我们</h2>
            <p class="section-subtitle">传承茶文化精髓，以匠心工艺打造每一杯优质茶饮</p>
          </div>
          
          <div class="about-grid">
            <!-- Brand Heritage -->
            <div class="about-panel heritage-panel">
              <div class="panel-background">
                <div class="heritage-illustration">
                  <div class="mountain-silhouette"></div>
                  <div class="tea-leaves floating-1"></div>
                  <div class="tea-leaves floating-2"></div>
                  <div class="tea-leaves floating-3"></div>
                  <div class="sunrise-circle"></div>
                </div>
              </div>
              <div class="panel-content">
                <div class="panel-header">
                  <span class="panel-category">BRAND HERITAGE</span>
                  <h2 class="panel-title">品牌历程</h2>
                </div>
                <div class="panel-details">
                  <p class="panel-description">
                    茶百道成立于2008年，历经15个春秋的发展历程。在这漫长的发展时间里，我们深度了解市场发展方向，
                    敏锐洞察消费者口味变化，不断满足消费者的新需求，打造出每一款都备受喜爱的优质茶饮。
                  </p>
                  <div class="panel-stats">
                    <div class="stat-item">
                      <span class="stat-number">2008</span>
                      <span class="stat-label">创立年份</span>
                    </div>
                    <div class="stat-item">
                      <span class="stat-number">15+</span>
                      <span class="stat-label">发展年限</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Panda Culture -->
            <div class="about-panel culture-panel">
              <div class="panel-background">
                <div class="culture-illustration">
                  <div class="panda-shape"></div>
                  <div class="bamboo-1"></div>
                  <div class="bamboo-2"></div>
                  <div class="culture-dots dot-1"></div>
                  <div class="culture-dots dot-2"></div>
                  <div class="culture-dots dot-3"></div>
                </div>
              </div>
              <div class="panel-content">
                <div class="panel-header">
                  <span class="panel-category">PANDA CULTURE</span>
                  <h2 class="panel-title">熊猫元素</h2>
                </div>
                <div class="panel-details">
                  <p class="panel-description">
                    风靡成都的茶百道将熊猫元素融入品牌文化，憨态可掬的丁丁猫形象深入人心。
                    特色饮品加特别的成都元素，深受年轻时尚人士的喜爱，得到了消费者们的一致好评。
                  </p>
                  <div class="panel-features">
                    <span class="feature-tag">成都文化</span>
                    <span class="feature-tag">熊猫IP</span>
                    <span class="feature-tag">年轻化</span>
                  </div>
                </div>
              </div>
            </div>

            <!-- Quality Craftsmanship -->
            <div class="about-panel quality-panel">
              <div class="panel-background">
                <div class="quality-illustration">
                  <div class="tea-cup"></div>
                  <div class="steam-lines line-1"></div>
                  <div class="steam-lines line-2"></div>
                  <div class="steam-lines line-3"></div>
                  <div class="quality-star star-1"></div>
                  <div class="quality-star star-2"></div>
                  <div class="quality-star star-3"></div>
                </div>
              </div>
              <div class="panel-content">
                <div class="panel-header">
                  <span class="panel-category">QUALITY CRAFT</span>
                  <h2 class="panel-title">品质匠心</h2>
                </div>
                <div class="panel-details">
                  <p class="panel-description">
                    遍访高山寻觅好茶，精选优质茶底，发挥出茶饮的无限想象。从严格挑选的茗茶，
                    到您手中的饮品，还要经过上百次的配比调试，以百分之百的热情去创造出独特、健康且美味的茶饮。
                  </p>
                  <div class="quality-metrics">
                    <div class="metric-item">
                      <span class="metric-number">100+</span>
                      <span class="metric-label">配比调试</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Brand Mission -->
            <div class="about-panel mission-panel">
              <div class="panel-background">
                <div class="mission-illustration">
                  <div class="heart-shape"></div>
                  <div class="mission-waves wave-1"></div>
                  <div class="mission-waves wave-2"></div>
                  <div class="mission-waves wave-3"></div>
                  <div class="mission-particles particle-1"></div>
                  <div class="mission-particles particle-2"></div>
                  <div class="mission-particles particle-3"></div>
                </div>
              </div>
              <div class="panel-content">
                <div class="panel-header">
                  <span class="panel-category">BRAND MISSION</span>
                  <h2 class="panel-title">品牌使命</h2>
                </div>
                <div class="panel-details">
                  <blockquote class="mission-quote">
                    "让年轻人爱上中国茶"
                  </blockquote>
                  <p class="panel-description">
                    茶百道致力于传承千年茶文化精髓，通过现代创新工艺，
                    让传统中国茶文化焕发新的活力，为年轻一代带来独特的茶饮文化体验。
                  </p>
                  <div class="mission-values">
                    <div class="value-item">传承</div>
                    <div class="value-item">创新</div>
                    <div class="value-item">体验</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts" setup>
import { gsap } from 'gsap';
import { ScrollToPlugin } from 'gsap/ScrollToPlugin';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
import { TextPlugin } from 'gsap/TextPlugin';
import { nextTick, onMounted, ref } from 'vue';

// 注册GSAP插件
gsap.registerPlugin(ScrollTrigger, ScrollToPlugin, TextPlugin);

// 导航状态
const activeSection = ref('hero');

// 统一轮播配置
const sliderConfigs = {
  products: { 
    current: ref(0), 
    total: 4, 
    touchStart: ref(0), 
    touchEnd: ref(0),
    selector: '.products-slider', 
    itemWidth: 25, 
    navSelector: '.nav-counter',
    dotsSelector: '.nav-dot'
  },
  stores: { 
    current: ref(0), 
    total: 3, 
    touchStart: ref(0), 
    touchEnd: ref(0),
    selector: '.stores-slider', 
    itemWidth: 33.333, 
    navSelector: '.stores-navigation .nav-counter',
    dotsSelector: '.stores-navigation .nav-dot'
  }
};

// 统一轮播控制方法
function navigateSlider(type: 'products' | 'stores', direction: 'next' | 'prev' | number) {
  const config = sliderConfigs[type];
  
  if (typeof direction === 'number') {
    config.current.value = direction;
  } else if (direction === 'next') {
    config.current.value = (config.current.value + 1) % config.total;
  } else {
    config.current.value = config.current.value === 0 ? config.total - 1 : config.current.value - 1;
  }
  
  updateSliderAnimation(type);
}

function updateSliderAnimation(type: 'products' | 'stores') {
  const config = sliderConfigs[type];
  const sliderElement = document.querySelector(config.selector) as HTMLElement;
  const counter = document.querySelector(config.navSelector);
  
  if (sliderElement) {
    const translateX = -config.current.value * config.itemWidth;
    gsap.to(sliderElement, { x: `${translateX}%`, duration: 0.6, ease: 'power2.inOut' });
  }
  
  if (counter) {
    gsap.to(counter, {
      scale: 1.2, duration: 0.2, ease: 'power2.out', yoyo: true, repeat: 1,
      onComplete: () => {
        counter.textContent = `${config.current.value + 1}/${config.total}`;
      }
    });
  }
  
  updateDotsAnimation(type);
}

function updateDotsAnimation(type: 'products' | 'stores') {
  const config = sliderConfigs[type];
  const dots = document.querySelectorAll(config.dotsSelector);
  
  dots.forEach((dot, index) => {
    const isActive = index === config.current.value;
    dot.classList.toggle('active', isActive);
    
    if (isActive) {
      gsap.fromTo(dot, { scale: 0.8, opacity: 0.5 }, { scale: 1.2, opacity: 1, duration: 0.3, ease: 'back.out(1.7)' });
    } else {
      gsap.to(dot, { scale: 1, opacity: 0.6, duration: 0.3, ease: 'power2.out' });
    }
  });
}

// 触摸处理
function handleTouch(type: 'products' | 'stores', action: 'start' | 'move' | 'end', e?: TouchEvent) {
  const config = sliderConfigs[type];
  
  switch (action) {
    case 'start':
      config.touchStart.value = e!.touches[0].clientX;
      break;
    case 'move':
      config.touchEnd.value = e!.touches[0].clientX;
      break;
    case 'end':
      if (!config.touchStart.value || !config.touchEnd.value) return;
      const difference = config.touchStart.value - config.touchEnd.value;
      const threshold = 50;
      
      if (Math.abs(difference) > threshold) {
        navigateSlider(type, difference > 0 ? 'next' : 'prev');
      }
      
      config.touchStart.value = 0;
      config.touchEnd.value = 0;
      break;
  }
}

// 简化的公开方法
const nextSlide = () => navigateSlider('products', 'next');
const prevSlide = () => navigateSlider('products', 'prev');
const goToSlide = (index: number) => navigateSlider('products', index);
const nextStore = () => navigateSlider('stores', 'next');
const prevStore = () => navigateSlider('stores', 'prev');
const goToStore = (index: number) => navigateSlider('stores', index);

const handleTouchStart = (e: TouchEvent) => handleTouch('products', 'start', e);
const handleTouchMove = (e: TouchEvent) => handleTouch('products', 'move', e);
const handleTouchEnd = () => handleTouch('products', 'end');
const handleStoreTouchStart = (e: TouchEvent) => handleTouch('stores', 'start', e);
const handleStoreTouchMove = (e: TouchEvent) => handleTouch('stores', 'move', e);
const handleStoreTouchEnd = () => handleTouch('stores', 'end');

// 导航菜单点击处理
function handleNavClick(event: Event) {
  event.preventDefault();
  const target = event.target as HTMLAnchorElement;
  const href = target.getAttribute('href');
  if (href && href.startsWith('#')) {
    const sectionId = href.substring(1);
    scrollToSection(sectionId);
  }
}

// 滚动到指定section
function scrollToSection(sectionId: string) {
  const targetElement = document.getElementById(sectionId);
  if (targetElement) {
    // 使用GSAP实现平滑滚动
    gsap.to(window, {
      duration: 1.2,
      scrollTo: {
        y: targetElement,
        offsetY: 80 // 考虑固定导航栏的高度
      },
      ease: 'power2.inOut'
    });
  }
}

onMounted(() => {
  // 等待DOM完全加载
  nextTick(() => {
    initGSAPAnimations();
    setupSliders();
  });
});

// 动画配置
const animationConfig = {
  hero: [
    { selector: '.hero-tags', from: { opacity: 0, y: 30 }, to: { opacity: 1, y: 0, duration: 0.8, ease: 'power2.out' } },
    { selector: '.title-line-1', from: { opacity: 0, x: -50 }, to: { opacity: 1, x: 0, duration: 1, ease: 'power3.out' }, offset: '-=0.3' },
    { selector: '.title-line-2', from: { opacity: 0, x: 50 }, to: { opacity: 1, x: 0, duration: 1, ease: 'power3.out' }, offset: '-=0.7' },
    { selector: '.hero-description', from: { opacity: 0, y: 30 }, to: { opacity: 1, y: 0, duration: 0.8, ease: 'power2.out' }, offset: '-=0.4' },
    { selector: '.hero-cta', from: { opacity: 0, scale: 0.8 }, to: { opacity: 1, scale: 1, duration: 0.6, ease: 'back.out(1.7)' }, offset: '-=0.2' },
    { selector: '.hero-subtitle', from: { opacity: 0, y: 20 }, to: { opacity: 1, y: 0, duration: 0.6, ease: 'power2.out' }, offset: '-=0.3' }
  ],
  scrollElements: [
    { selector: '.section-title', from: { opacity: 0, y: 50 }, to: { opacity: 1, y: 0, duration: 1, ease: 'power2.out' } },
    { selector: '.product-slide', from: { opacity: 0, y: 100 }, to: { opacity: 1, y: 0, duration: 0.8, ease: 'power2.out' } },
    { selector: '.about-panel', from: { scale: 0.8, opacity: 0 }, to: { scale: 1, opacity: 1, duration: 0.8, ease: 'back.out(1.7)' } }
  ]
};

// GSAP动画初始化
function initGSAPAnimations() {
  initHeroAnimations();
  initScrollAnimations();
  initInteractiveAnimations();
  enhanceExistingAnimations();
  setupNavActiveState();
}

function initHeroAnimations() {
  const tl = gsap.timeline();
  
  animationConfig.hero.forEach(({ selector, from, to, offset }) => {
    gsap.set(selector, from);
    tl.to(selector, to, offset || '');
  });
  
  gsap.set('.top-nav', { y: -100 });
  gsap.to('.top-nav', { y: 0, duration: 0.8, ease: 'power2.out', delay: 0.5 });
}

function initScrollAnimations() {
  // 通用滚动动画
  animationConfig.scrollElements.forEach(({ selector, from, to }) => {
    gsap.utils.toArray(selector).forEach((element, index) => {
      gsap.set(element as Element, from);
      
      ScrollTrigger.create({
        trigger: element as Element,
        start: 'top 85%',
        onEnter: () => {
          gsap.to(element as Element, { ...to, delay: index * 0.1 });
          if (selector === '.about-panel') {
            animatePanelElements(element as HTMLElement, index);
          }
        }
      });
    });
  });

  // 门店卡片特殊动画
  gsap.utils.toArray('.store-slide').forEach((slide, index) => {
    gsap.set(slide as Element, { opacity: 0, x: index % 2 === 0 ? -100 : 100 });
    ScrollTrigger.create({
      trigger: slide as Element,
      start: 'top 85%',
      onEnter: () => gsap.to(slide as Element, { opacity: 1, x: 0, duration: 0.8, ease: 'power2.out', delay: index * 0.2 })
    });
  });

  // 统计数字动画
  gsap.utils.toArray('.stat-number').forEach((number) => {
    const element = number as HTMLElement;
    const finalValue = element.textContent || '0';
    const numericValue = parseInt(finalValue.replace(/\D/g, '')) || 0;
    
    gsap.set(element, { textContent: '0' });
    ScrollTrigger.create({
      trigger: element,
      start: 'top 80%',
      onEnter: () => {
        gsap.to(element, {
          textContent: numericValue, duration: 2, ease: 'power2.out', snap: { textContent: 1 },
          onUpdate: function() {
            const currentValue = Math.ceil(this.targets()[0].textContent);
            element.textContent = finalValue.includes('+') ? currentValue + '+' :
                                finalValue.includes('H') ? currentValue + 'H' : currentValue.toString();
          }
        });
      }
    });
  });
}

function initInteractiveAnimations() {
  // 悬停动画
  const hoverElements = [
    { selector: '.cta-button, .hero-cta, .action-btn', hover: { scale: 1.05 }, normal: { scale: 1 } },
    { selector: '.product-image-container', hover: { rotationY: 5, rotationX: 5, scale: 1.05, transformPerspective: 1000 }, normal: { rotationY: 0, rotationX: 0, scale: 1 } }
  ];

  hoverElements.forEach(({ selector, hover, normal }) => {
    gsap.utils.toArray(selector).forEach((element) => {
      const el = element as HTMLElement;
      el.addEventListener('mouseenter', () => gsap.to(el, { ...hover, duration: 0.3, ease: 'power2.out' }));
      el.addEventListener('mouseleave', () => gsap.to(el, { ...normal, duration: 0.3, ease: 'power2.out' }));
    });
  });
}

// 增强面板内部动画
function animatePanelElements(panel: HTMLElement, index: number) {
  const delay = index * 0.1;
  
  // 根据面板类型添加特定动画
  if (panel.classList.contains('heritage-panel')) {
    gsap.to(panel.querySelector('.sunrise-circle'), {
      rotation: 360,
      duration: 20,
      ease: 'none',
      repeat: -1,
      delay: delay
    });
    
    gsap.utils.toArray(panel.querySelectorAll('.tea-leaves')).forEach((leaf, i) => {
      gsap.to(leaf as Element, {
        y: '+=20',
        rotation: '+=15',
        duration: 3 + i,
        ease: 'power1.inOut',
        repeat: -1,
        yoyo: true,
        delay: delay + i * 0.3
      });
    });
  }
  
  if (panel.classList.contains('culture-panel')) {
    gsap.to(panel.querySelector('.panda-shape'), {
      scale: 1.1,
      duration: 2,
      ease: 'power1.inOut',
      repeat: -1,
      yoyo: true,
      delay: delay
    });
  }
  
  if (panel.classList.contains('quality-panel')) {
    gsap.utils.toArray(panel.querySelectorAll('.steam-lines')).forEach((line, i) => {
      gsap.to(line as Element, {
        y: -30,
        opacity: 0,
        duration: 2,
        ease: 'power1.out',
        repeat: -1,
        delay: delay + i * 0.3
      });
    });
  }
  
  if (panel.classList.contains('mission-panel')) {
    gsap.to(panel.querySelector('.heart-shape'), {
      scale: 1.2,
      duration: 1.5,
      ease: 'power1.inOut',
      repeat: -1,
      yoyo: true,
      delay: delay
    });
  }
}

// 增强现有CSS动画
function enhanceExistingAnimations() {
  // 增强茶叶飘动
  gsap.utils.toArray('.floating-1, .floating-2, .floating-3').forEach((leaf, index) => {
    gsap.to(leaf as Element, {
      rotation: 360,
      duration: 10 + index * 2,
      ease: 'none',
      repeat: -1
    });
  });
  
  // 增强熊猫元素
  gsap.utils.toArray('.culture-dots').forEach((dot, index) => {
    gsap.to(dot as Element, {
      scale: 1.5,
      duration: 1.5 + index * 0.3,
      ease: 'power1.inOut',
      repeat: -1,
      yoyo: true
    });
  });
  
  // 增强质量星星
  gsap.utils.toArray('.quality-star').forEach((star, index) => {
    gsap.to(star as Element, {
      rotation: 360,
      duration: 5 + index,
      ease: 'none',
      repeat: -1
    });
  });
}

// 设置导航栏激活状态监听
function setupNavActiveState() {
  const sections = ['hero', 'products', 'stores', 'about'];
  
  sections.forEach((sectionId) => {
    const element = document.getElementById(sectionId);
    if (element) {
      ScrollTrigger.create({
        trigger: element,
        start: 'top 100px', // 当section顶部距离视口顶部100px时触发
        end: 'bottom 100px',
        onEnter: () => {
          activeSection.value = sectionId;
        },
        onEnterBack: () => {
          activeSection.value = sectionId;
        }
      });
    }
  });
}

// 设置轮播功能
function setupSliders() {
  // 产品轮播按钮
  const prevBtn = document.querySelector('.prev-btn');
  const nextBtn = document.querySelector('.next-btn');
  if (prevBtn) prevBtn.addEventListener('click', prevSlide);
  if (nextBtn) nextBtn.addEventListener('click', nextSlide);
  
  // 产品轮播指示点
  const dots = document.querySelectorAll('.nav-dot');
  dots.forEach((dot, index) => {
    dot.addEventListener('click', () => goToSlide(index));
  });
  
  // 产品轮播触摸
  const slider = document.querySelector('.products-showcase');
  if (slider) {
    slider.addEventListener('touchstart', handleTouchStart as EventListener, { passive: true });
    slider.addEventListener('touchmove', handleTouchMove as EventListener, { passive: true });
    slider.addEventListener('touchend', handleTouchEnd as EventListener, { passive: true });
  }
  
  // 门店轮播按钮
  const storePrevBtn = document.querySelector('.store-prev-btn');
  const storeNextBtn = document.querySelector('.store-next-btn');
  if (storePrevBtn) storePrevBtn.addEventListener('click', prevStore);
  if (storeNextBtn) storeNextBtn.addEventListener('click', nextStore);
  
  // 门店轮播指示点
  const storeDots = document.querySelectorAll('.stores-navigation .nav-dot');
  storeDots.forEach((dot, index) => {
    dot.addEventListener('click', () => goToStore(index));
  });
  
  // 门店轮播触摸
  const storeSlider = document.querySelector('.stores-showcase');
  if (storeSlider) {
    storeSlider.addEventListener('touchstart', handleStoreTouchStart as EventListener, { passive: true });
    storeSlider.addEventListener('touchmove', handleStoreTouchMove as EventListener, { passive: true });
    storeSlider.addEventListener('touchend', handleStoreTouchEnd as EventListener, { passive: true });
  }
}
</script>

<style>
:root {
  /* 主色调 */
  --primary-blue: #1e40af;
  --primary-blue-light: #3b82f6;
  --primary-blue-dark: #1d4ed8;
  --primary-blue-darker: #1e3a8a;
  --accent-yellow: #fbbf24;
  --accent-yellow-dark: #f59e0b;
  --accent-green: #10b981;
  
  /* 灰色系 */
  --gray-50: #f8fafc;
  --gray-100: #f1f5f9;
  --gray-200: #e2e8f0;
  --gray-300: #cbd5e1;
  --gray-400: #94a3b8;
  --gray-500: #64748b;
  --gray-600: #475569;
  --gray-700: #334155;
  --gray-800: #1e293b;
  --gray-900: #0f172a;
  
  /* 常用渐变 */
  --gradient-primary: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-blue-light) 100%);
  --gradient-primary-hover: linear-gradient(135deg, var(--primary-blue-dark) 0%, #2563eb 100%);
  --gradient-accent: linear-gradient(135deg, var(--accent-yellow) 0%, var(--accent-yellow-dark) 100%);
  --gradient-card: linear-gradient(135deg, rgba(255, 255, 255, 0.95) 0%, rgba(248, 250, 252, 0.9) 100%);
  --gradient-card-hover: linear-gradient(135deg, rgba(255, 255, 255, 0.98) 0%, rgba(240, 247, 255, 0.95) 100%);
  
  /* 阴影 */
  --shadow-sm: 0 4px 15px rgba(30, 64, 175, 0.2);
  --shadow-md: 0 4px 20px rgba(30, 64, 175, 0.08);
  --shadow-lg: 0 8px 30px rgba(30, 64, 175, 0.12);
  --shadow-xl: 0 12px 40px rgba(0, 0, 0, 0.15);
  
  /* 边框半径 */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-full: 50%;
  
  /* 间距 */
  --space-xs: 0.5rem;
  --space-sm: 0.8rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2rem;
  --space-2xl: 3rem;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
  overflow-x: hidden;
}

#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', '微软雅黑', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: linear-gradient(180deg, #dbeafe 0%, #f0f7ff 50%, #e6f3ff 100%);
  min-height: 100vh;
}

/* Top Navigation Styles */
.top-nav {
  background: linear-gradient(180deg, 
    rgba(248, 250, 252, 0.95) 0%, 
    rgba(240, 247, 255, 0.9) 40%, 
    rgba(219, 234, 254, 0.85) 100%);
  backdrop-filter: blur(15px);
  border-bottom: 1px solid rgba(30, 64, 175, 0.2);
  padding: 0 2rem;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 4px 25px rgba(30, 64, 175, 0.15);
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
}

/* Logo Styles */
.logo {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  cursor: pointer;
  transition: all 0.3s ease;
}

.logo:hover {
  transform: translateY(-1px);
}

.logo-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
  transition: all 0.3s ease;
}

.logo-icon:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 15px rgba(30, 64, 175, 0.2);
}

.logo-text {
  font-size: 1.4rem;
  font-weight: bold;
  color: #1e40af;
  text-decoration: none;
  letter-spacing: 1px;
}

/* Navigation Menu */
.nav-menu {
  display: flex;
  align-items: center;
  gap: 2.5rem;
}

.nav-link {
  color: #334155;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.95rem;
  transition: all 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: #1e40af;
}

.nav-link:hover::after,
.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, #1e40af, #3b82f6);
  border-radius: 1px;
}

.nav-link.active {
  color: #1e40af;
  font-weight: 600;
}

.nav-link.active::after {
  opacity: 1;
  animation: activeBorder 0.3s ease;
}

@keyframes activeBorder {
  from {
    width: 0;
    opacity: 0;
  }
  to {
    width: 100%;
    opacity: 1;
  }
}

/* CTA Button */
.cta-button {
  background: var(--gradient-primary);
  color: white;
  border: none;
  padding: 0.75rem 1.8rem;
  border-radius: 25px;
  font-weight: 600;
  font-size: 0.9rem;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: var(--shadow-sm);
}

.cta-button:hover {
  background: var(--gradient-primary-hover);
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(30, 64, 175, 0.3);
}

/* Main Content */
.main-content {
  padding: 0;
  max-width: 100%;
  margin: 0;
}

.hero-section {
  position: relative;
  width: 100%;
  height: 100vh;
  min-height: 600px;
  background: linear-gradient(135deg, #314a9a 0%, #3e639e 50%, #1e40af 100%);
  background-image: url('/cha-index.png');
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(
    135deg,
    rgba(30, 64, 175, 0.7) 0%,
    rgba(59, 130, 246, 0.6) 50%,
    rgba(30, 64, 175, 0.8) 100%
  );
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  text-align: center;
  color: white;
  max-width: 900px;
  padding: 0 2rem;
}

.hero-tags {
  margin-bottom: 3rem;
  font-size: 1.3rem;
  font-weight: 500;
  letter-spacing: 3px;
  text-transform: uppercase;
  opacity: 0.9;
}

.tag {
  color: #cbd5e1;
  padding: 0 0.5rem;
}

.tag-separator {
  color: #64748b;
  margin: 0 1rem;
}

.hero-title {
  margin-bottom: 2.5rem;
  line-height: 1.1;
}

.title-line-1 {
  font-size: 4.8rem;
  font-weight: 600;
  color: #60a5fa;
  margin-bottom: 0.5rem;
  letter-spacing: 2px;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}

.title-line-2 {
  font-size: 6.5rem;
  font-weight: 800;
  color: #ffffff;
  letter-spacing: 3px;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
}

.hero-description {
  font-size: 1.8rem;
  font-weight: 400;
  margin-bottom: 3.5rem;
  line-height: 1.7;
  letter-spacing: 1px;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
  color: #e2e8f0;
  opacity: 0.95;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.hero-cta {
  background: var(--gradient-accent);
  color: #1f2937;
  border: none;
  padding: 1.4rem 3.5rem;
  border-radius: 30px;
  font-weight: 700;
  font-size: 1.5rem;
  cursor: pointer;
  transition: all 0.4s ease;
  box-shadow: 0 8px 25px rgba(251, 191, 36, 0.3);
  text-transform: uppercase;
  letter-spacing: 2px;
  display: inline-flex;
  align-items: center;
  gap: var(--space-sm);
  margin-bottom: var(--space-2xl);
}

.hero-cta:hover {
  background: linear-gradient(135deg, var(--accent-yellow-dark) 0%, #d97706 100%);
  transform: translateY(-3px);
  box-shadow: 0 12px 35px rgba(251, 191, 36, 0.4);
}

.hero-cta svg {
  transition: transform 0.3s ease;
}

.hero-cta:hover svg {
  transform: translateX(3px);
}

.hero-subtitle {
  font-size: 1.4rem;
  font-weight: 400;
  color: #94a3b8;
  letter-spacing: 1px;
  opacity: 0.8;
}

.trust-text {
  color: #cbd5e1;
}

.highlight-number {
  color: #fbbf24;
  font-weight: 700;
  font-size: 1.8rem;
  margin: 0 0.5rem;
}

/* 平板和手机通用样式 */
@media (max-width: 768px) {
  .nav-container { padding: 0 1rem; }
  .nav-menu { gap: 1.5rem; }
  .nav-link { font-size: 0.9rem; }
  .cta-button { padding: 0.6rem 1.4rem; font-size: 0.85rem; }
  .logo-icon { width: 50px; height: 50px; }
  
  .hero-section { height: 100vh; min-height: 500px; }
  .hero-tags { margin-bottom: 2rem; font-size: 1.2rem; letter-spacing: 2px; }
  .tag-separator { margin: 0 0.8rem; }
  .title-line-1 { font-size: 3.5rem; letter-spacing: 1px; }
  .title-line-2 { font-size: 4.5rem; letter-spacing: 2px; }
  .hero-description { font-size: 1.6rem; margin-bottom: 2.5rem; line-height: 1.6; }
  .hero-cta { padding: 1.2rem 2.8rem; font-size: 1.4rem; letter-spacing: 1px; margin-bottom: 2.5rem; }
  .hero-subtitle { font-size: 1.3rem; }
  .highlight-number { font-size: 1.6rem; }
}

/* Products Section */
.products-section {
  background: linear-gradient(180deg, #e2e8f0 0%, #ffffff 30%, #f8fafc 80%, #f1f5f9 100%);
  padding: 4rem 0;
  position: relative;
}

.products-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 40%;
  height: 100%;
  background-image: url('/cha-product-index.png');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  opacity: 0.06;
  pointer-events: none;
  z-index: 1;
}

.products-section::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 40%;
  height: 100%;
  background: linear-gradient(
    135deg,
    rgba(30, 64, 175, 0.02) 0%,
    rgba(59, 130, 246, 0.01) 50%,
    transparent 100%
  );
  pointer-events: none;
  z-index: 1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  position: relative;
  z-index: 2;
}

.section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.section-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: #1e40af;
  margin-bottom: 1.5rem;
  letter-spacing: 2px;
}

.section-subtitle {
  font-size: 1.3rem;
  color: #64748b;
  font-weight: 400;
  letter-spacing: 1px;
  line-height: 1.6;
}

.products-showcase {
  margin-bottom: 4rem;
  overflow: hidden;
}

.products-slider {
  display: flex;
  transition: transform 0.5s ease;
  width: 400%; /* 4 products = 400% */
}

.product-slide {
  flex: 0 0 25%; /* Each slide takes 25% of the slider width */
  width: 25%;
}

.product-feature {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: center;
  padding: 1.5rem 2rem;
  min-height: 480px;
}

.product-feature.reverse {
  direction: rtl;
}

.product-feature.reverse > * {
  direction: ltr;
}

.product-image-container {
  position: relative;
  border-radius: 20px;
  overflow: visible;
  background: transparent;
  transition: all 0.4s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.product-image-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    linear-gradient(135deg, 
      rgba(255, 255, 255, 0.95) 0%, 
      rgba(248, 250, 252, 0.9) 50%, 
      rgba(241, 245, 249, 0.95) 100%);
  border-radius: 20px;
  box-shadow: 
    0 20px 60px rgba(30, 64, 175, 0.08),
    0 8px 30px rgba(0, 0, 0, 0.04);
  border: 1px solid rgba(30, 64, 175, 0.06);
  z-index: 1;
}

.product-image-container:hover {
  transform: translateY(-5px);
  background: 
    radial-gradient(circle at 30% 20%, rgba(59, 130, 246, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 70% 80%, rgba(147, 197, 253, 0.12) 0%, transparent 50%),
    linear-gradient(135deg, rgba(255, 255, 255, 0.95) 0%, rgba(248, 250, 252, 1) 100%);
  box-shadow: 
    0 25px 80px rgba(30, 64, 175, 0.15),
    inset 0 1px 0 rgba(255, 255, 255, 0.6);
  border-color: rgba(30, 64, 175, 0.12);
}

.product-image {
  width: 100%;
  height: 320px;
  object-fit: contain;
  border-radius: 20px;
  padding: 1rem;
  position: relative;
  z-index: 2;
  mix-blend-mode: multiply;
  filter: 
    drop-shadow(0 8px 16px rgba(0, 0, 0, 0.1))
    brightness(1.05)
    contrast(1.1);
  transition: all 0.3s ease;
}

.product-image:hover {
  transform: scale(1.02);
  filter: 
    drop-shadow(0 12px 20px rgba(0, 0, 0, 0.15))
    brightness(1.1)
    contrast(1.15);
}

.product-content {
  padding: var(--space-xl);
  background: var(--gradient-card);
  border: 1px solid rgba(30, 64, 175, 0.1);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.product-content:hover {
  background: var(--gradient-card-hover);
  border-color: rgba(30, 64, 175, 0.15);
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}

.product-category {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--primary-blue-light);
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: var(--space-md);
}

.product-title {
  font-size: 2.2rem;
  font-weight: 700;
  color: var(--primary-blue);
  margin-bottom: var(--space-lg);
  letter-spacing: 1px;
  line-height: 1.2;
}

.product-quote {
  margin-bottom: 1.8rem;
}

.product-quote blockquote {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #374151;
  font-style: italic;
  position: relative;
  padding-left: 2rem;
  border-left: 4px solid #3b82f6;
  margin: 0;
}

.product-quote blockquote::before {
  content: '"';
  font-size: 4rem;
  color: #3b82f6;
  position: absolute;
  left: -1rem;
  top: -1rem;
  font-family: serif;
}

.product-details {
  margin-bottom: 1.8rem;
}

.detail-item {
  display: flex;
  align-items: center;
  margin-bottom: 0.6rem;
  font-size: 0.95rem;
}

.detail-label {
  font-weight: 600;
  color: #1e40af;
  min-width: 80px;
}

.detail-value {
  color: #64748b;
  font-weight: 500;
}

.brand-mark {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding-top: 1.5rem;
  border-top: 1px solid #e2e8f0;
}

.brand-logo {
  font-size: 1.2rem;
  font-weight: 700;
  color: #1e40af;
  background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
  padding: 0.5rem 1rem;
  border-radius: 8px;
}

.brand-desc {
  font-size: 0.9rem;
  color: #64748b;
  font-style: italic;
}

.products-navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 2rem;
  padding-top: 1.5rem;
  border-top: 1px solid #e2e8f0;
}

.nav-counter {
  font-size: 1.1rem;
  font-weight: 600;
  color: #64748b;
}

.nav-dots {
  display: flex;
  gap: 0.8rem;
}

.nav-dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #cbd5e1;
  cursor: pointer;
  transition: all 0.3s ease;
}

.nav-dot.active {
  background: #3b82f6;
  transform: scale(1.2);
}

.nav-dot:hover {
  background: #64748b;
}

.nav-buttons {
  display: flex;
  gap: 1rem;
}

.nav-btn {
  width: 50px;
  height: 50px;
  border: 2px solid #e2e8f0;
  background: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.3s ease;
  color: #64748b;
}

.nav-btn:hover {
  border-color: #3b82f6;
  color: #3b82f6;
  transform: translateY(-2px);
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.2);
}

/* Products Section Responsive */
@media (max-width: 768px) {
  .products-section {
    padding: 3rem 0;
  }
  
  .products-section::before {
    width: 35%;
    opacity: 0.06;
  }
  
  .section-header {
    margin-bottom: 2rem;
  }
  
  .section-title {
    font-size: 2.2rem;
    letter-spacing: 1px;
  }
  
  .section-subtitle {
    font-size: 1.1rem;
  }
  
  .products-slider {
    width: 400%; /* Keep horizontal scroll on tablet */
  }
  
  .product-feature {
    grid-template-columns: 1fr;
    gap: 2rem;
    padding: 1rem;
    min-height: auto;
  }
  
  .product-content {
    padding: 1.5rem;
    border-radius: 12px;
  }
  
  .product-feature.reverse {
    direction: ltr;
  }
  
  .product-image {
    height: 250px;
    padding: 0.8rem;
  }
  
  .product-title {
    font-size: 1.8rem;
    margin-bottom: 1rem;
  }
  
  .product-quote {
    margin-bottom: 1.2rem;
  }
  
  .product-quote blockquote {
    font-size: 1rem;
    padding-left: 1.5rem;
  }
  
  .product-quote blockquote::before {
    font-size: 2.5rem;
    left: -0.8rem;
    top: -0.8rem;
  }
  
  .product-details {
    margin-bottom: 1.2rem;
  }
  
  .brand-mark {
    padding-top: 1rem;
  }
  
  .products-navigation {
    margin-top: 1.5rem;
    padding-top: 1rem;
  }
  
  .nav-btn {
    width: 45px;
    height: 45px;
  }
  
  .nav-dots {
    gap: 0.6rem;
  }
  
  .nav-dot {
    width: 10px;
    height: 10px;
  }
}

/* 手机端优化 */
@media (max-width: 480px) {
  .nav-container {
    flex-direction: column;
    height: auto;
    padding: var(--space-md) 0;
    gap: var(--space-md);
  }
  .nav-menu { 
    display: flex; 
    gap: var(--space-sm);
    flex-wrap: wrap;
    justify-content: center;
  }
  .nav-link { 
    font-size: 0.8rem; 
    padding: 0.3rem 0.6rem;
    white-space: nowrap;
  }
  .cta-button { 
    padding: var(--space-xs) var(--space-md); 
    font-size: 0.8rem;
    white-space: nowrap;
  }
  .logo { gap: var(--space-xs); }
  .logo-icon { width: 45px; height: 45px; }
  .container { padding: 0 var(--space-sm); }
  
  .store-slide {
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
    overflow: hidden;
    flex: 0 0 33.333%;
  }
  
  .stores-slider {
    display: flex;
    width: 300%;
    box-sizing: border-box;
  }
  
  .section-header { margin-bottom: 1.5rem; }
  .section-title { font-size: 1.8rem; }
  .section-subtitle { font-size: 0.95rem; }
  
  .hero-section { height: 100vh; min-height: 450px; }
  .hero-content { padding: 0 1rem; }
  .hero-tags { margin-bottom: 1.5rem; font-size: 1.1rem; letter-spacing: 1px; }
  .tag-separator { margin: 0 0.5rem; }
  .title-line-1 { font-size: 2.8rem; letter-spacing: 1px; margin-bottom: 0.3rem; }
  .title-line-2 { font-size: 3.6rem; letter-spacing: 1px; }
  .hero-description { font-size: 1.4rem; margin-bottom: 2rem; padding: 0 0.5rem; }
  .hero-cta { padding: 1rem 2.2rem; font-size: 1.3rem; letter-spacing: 1px; margin-bottom: 2rem; }
  .hero-cta svg { width: 18px; height: 18px; }
  .hero-subtitle { font-size: 1.2rem; padding: 0 1rem; }
  .highlight-number { font-size: 1.5rem; }
  
  .products-section { padding: 2rem 0; }
  .products-section::before { width: 30%; opacity: 0.05; }
  .product-feature { grid-template-columns: 1fr; gap: 1.5rem; padding: 1rem; min-height: auto; }
  .product-feature.reverse { direction: ltr; }
  .product-image { height: 220px; border-radius: 15px; padding: 1rem; }
  .product-content { padding: 1.5rem; border-radius: 12px; box-shadow: 0 2px 15px rgba(30, 64, 175, 0.06); }
  .product-title { font-size: 1.6rem; margin-bottom: 1rem; }
  .product-quote { margin-bottom: 1.2rem; }
  .product-quote blockquote { font-size: 1rem; padding-left: 1.5rem; }
  .product-quote blockquote::before { font-size: 2.5rem; left: -0.8rem; top: -0.6rem; }
  .detail-item { font-size: 0.9rem; margin-bottom: 0.5rem; }
  .detail-label { min-width: 70px; }
  
  .products-navigation { flex-direction: column; gap: 1rem; margin-top: 1.5rem; padding-top: 1rem; }
  .nav-dots { order: -1; }
  .nav-dot { width: 10px; height: 10px; }
  .nav-btn { width: 40px; height: 40px; }
}



/* Stores Section */
.stores-section {
  background: linear-gradient(180deg, #f1f5f9 0%, #e2e8f0 25%, #64748b 70%, #334155 100%);
  padding: 4rem 0;
  position: relative;
}

.stores-section::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 40%;
  height: 100%;
  background-image: url('/cha-product-index.png');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  opacity: 0.05;
  pointer-events: none;
  z-index: 1;
  transform: scaleX(-1);
}

.stores-main-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 3rem;
  align-items: stretch;
  min-height: 500px;
}

.stores-left {
  width: 100%;
}

.stores-showcase {
  margin-bottom: 2rem;
  overflow: hidden;
}

.stores-slider {
  display: flex;
  transition: transform 0.5s ease;
  width: 300%; /* 3 stores = 300% */
}

.store-slide {
  flex: 0 0 33.333%; /* Each slide takes 33.333% of the slider width */
  width: 33.333%;
}

.store-feature {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: center;
  padding: 2rem;
  min-height: 450px;
}

.stores-right {
  height: 100%;
  display: flex;
}

.store-feature.reverse {
  direction: rtl;
}

.store-feature.reverse > * {
  direction: ltr;
}

.store-image-container {
  position: relative;
  border-radius: 20px;
  overflow: visible;
  background: transparent;
  transition: all 0.4s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.store-image-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    linear-gradient(135deg, 
      rgba(255, 255, 255, 0.95) 0%, 
      rgba(248, 250, 252, 0.9) 50%, 
      rgba(241, 245, 249, 0.95) 100%);
  border-radius: 20px;
  box-shadow: 
    0 20px 60px rgba(30, 64, 175, 0.08),
    0 8px 30px rgba(0, 0, 0, 0.04);
  border: 1px solid rgba(30, 64, 175, 0.06);
  z-index: 1;
}

.store-image-container:hover {
  transform: translateY(-5px);
}

.store-image-container:hover::before {
  box-shadow: 
    0 25px 80px rgba(30, 64, 175, 0.12),
    0 12px 40px rgba(0, 0, 0, 0.06);
}

.store-image {
  width: 100%;
  height: 350px;
  object-fit: cover;
  border-radius: 20px;
  position: relative;
  z-index: 2;
  transition: all 0.3s ease;
}

.store-overlay {
  position: absolute;
  top: 1rem;
  right: 1rem;
  z-index: 3;
}

.status-badge {
  background: #10b981;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  box-shadow: 0 4px 15px rgba(16, 185, 129, 0.3);
}

.store-content {
  padding: var(--space-xl);
  background: var(--gradient-card);
  border: 1px solid rgba(30, 64, 175, 0.1);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
}

.store-content:hover {
  background: var(--gradient-card-hover);
  border-color: rgba(30, 64, 175, 0.15);
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}

.store-location {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  margin-bottom: 1rem;
}

.city-name {
  font-size: 1rem;
  font-weight: 600;
  color: #3b82f6;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.store-title {
  font-size: 2rem;
  font-weight: 700;
  color: #1e40af;
  margin-bottom: 1rem;
  letter-spacing: 1px;
  line-height: 1.2;
}

.store-address {
  margin-bottom: 1.5rem;
}

.store-address p {
  font-size: 1rem;
  color: #64748b;
  line-height: 1.5;
}

.store-features {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin-bottom: 1.5rem;
}

.feature-tag {
  background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
  color: #1e40af;
  padding: 0.4rem 0.8rem;
  border-radius: 15px;
  font-size: 0.8rem;
  font-weight: 600;
  border: 1px solid rgba(30, 64, 175, 0.1);
}

.store-details {
  margin-bottom: 2rem;
}

.detail-row {
  display: flex;
  align-items: center;
  margin-bottom: 0.6rem;
  font-size: 0.9rem;
}

.detail-label {
  font-weight: 600;
  color: #1e40af;
  min-width: 100px;
}

.detail-value {
  color: #64748b;
  font-weight: 500;
}

.store-actions {
  display: flex;
  gap: 1rem;
}

.action-btn {
  padding: 0.8rem 1.5rem;
  border-radius: 8px;
  font-weight: 600;
  font-size: 0.9rem;
  cursor: pointer;
  transition: all 0.3s ease;
  border: none;
}

.action-btn.primary {
  background: var(--gradient-primary);
  color: white;
  box-shadow: var(--shadow-sm);
}

.action-btn.primary:hover {
  background: var(--gradient-primary-hover);
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(30, 64, 175, 0.3);
}

.action-btn.secondary {
  background: white;
  color: var(--primary-blue);
  border: 2px solid var(--primary-blue);
}

.action-btn.secondary:hover {
  background: var(--primary-blue);
  color: white;
  transform: translateY(-2px);
  box-shadow: var(--shadow-sm);
}

.stores-navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1rem;
  padding-top: 1rem;
  border-top: 1px solid #e2e8f0;
}

.stores-summary {
  background: transparent;
  border-radius: 16px;
  padding: 0;
  border: none;
  box-shadow: none;
  overflow: hidden;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.summary-header {
  background: transparent;
  color: white;
  text-align: center;
  padding: 1.5rem 1.5rem 1.2rem;
  margin-bottom: 0;
}

.summary-title {
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 0.3rem;
  letter-spacing: 0.5px;
  color: white;
}

.summary-subtitle {
  font-size: 0.85rem;
  color: rgba(255, 255, 255, 0.9);
  font-weight: 400;
  line-height: 1.3;
}

.summary-stats {
  padding: 1.5rem 1.2rem;
  background: transparent;
  margin-bottom: 0;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 300px;
  gap: 1rem;
}

.stat-item {
  text-align: center;
  padding: 2rem 1.2rem;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.95) 0%, rgba(248, 250, 252, 0.9) 100%);
  border-radius: 16px;
  border: 2px solid rgba(30, 64, 175, 0.2);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15), 0 4px 12px rgba(30, 64, 175, 0.1);
  backdrop-filter: blur(20px);
  transition: all 0.4s ease;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.stat-item:hover {
  transform: translateY(-6px) scale(1.02);
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.98) 0%, rgba(240, 247, 255, 0.95) 100%);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2), 0 8px 20px rgba(30, 64, 175, 0.2);
  border-color: rgba(30, 64, 175, 0.4);
}

.stat-number {
  font-size: 3.5rem;
  font-weight: 900;
  color: #1e40af;
  margin-bottom: 0.4rem;
  letter-spacing: -2px;
  line-height: 0.9;
  text-shadow: 0 3px 6px rgba(0, 0, 0, 0.15);
  background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.stat-label {
  font-size: 1rem;
  color: #0f172a;
  font-weight: 700;
  letter-spacing: 0.5px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
}



/* Stores Section Responsive */
@media (max-width: 1024px) {
  .stores-section {
    padding: 3rem 0;
  }
  
  .stores-section::before {
    width: 30%;
    opacity: 0.04;
  }
  
  .stores-main-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .stores-right {
    height: auto;
  }
  
  .stores-summary {
    height: auto;
  }
  
  .summary-stats {
    flex: none;
    justify-content: flex-start;
    gap: 1rem;
  }
  
  .store-feature {
    padding: 1.5rem;
    min-height: 400px;
  }
  
  .store-image {
    height: 300px;
  }
  
  .store-content {
    padding: 1.8rem;
  }
  
  .store-title {
    font-size: 1.8rem;
  }
}

@media (max-width: 768px) {
  .stores-section {
    padding: 3rem 0;
  }
  
  .stores-section::before {
    width: 25%;
    opacity: 0.04;
  }
  
  .stores-slider {
    width: 300%; /* Keep horizontal scroll on tablet */
  }
  
  .store-feature {
    grid-template-columns: 1fr 1fr; /* 保持左右布局 */
    gap: 1.5rem;
    padding: 1.2rem;
    min-height: 350px;
  }
  
  .store-feature.reverse {
    direction: rtl; /* 保持反向布局 */
  }
  
  .store-feature.reverse > * {
    direction: ltr;
  }
  
  .store-image {
    height: 220px;
  }
  
  .store-content {
    padding: 1.5rem;
  }
  
  .store-title {
    font-size: 1.5rem;
  }
  
  .store-actions {
    flex-direction: column;
    gap: 0.8rem;
  }
  
  .action-btn {
    width: 100%;
    padding: 0.7rem 1.2rem;
    font-size: 0.9rem;
  }
  
  .stores-summary {
    border-radius: 12px;
  }
  
  .summary-header {
    padding: 1.2rem 1rem 1rem;
  }
  
  .summary-title {
    font-size: 1.3rem;
  }
  
  .summary-stats {
    padding: 1.2rem 1rem;
    min-height: 250px;
    gap: 0.8rem;
    background: transparent;
  }
  
  .stat-item {
    padding: 1.5rem 1rem;
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.92) 0%, rgba(248, 250, 252, 0.88) 100%);
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12), 0 3px 10px rgba(30, 64, 175, 0.08);
    border: 1.5px solid rgba(30, 64, 175, 0.15);
  }
  
  .stat-number {
    font-size: 2.8rem;
    letter-spacing: -1px;
  }
  
  .stat-label {
    font-size: 0.9rem;
  }
}

/* 针对中等屏幕尺寸的优化 */
@media (max-width: 600px) {
  .store-feature {
    grid-template-columns: 1fr 1fr; /* 继续保持左右布局 */
    gap: 1rem;
    padding: 1rem;
    min-height: 320px;
  }
  
  .store-image {
    height: 180px;
  }
  
  .store-content {
    padding: 1.2rem;
  }
  
  .store-title {
    font-size: 1.3rem;
    margin-bottom: 0.8rem;
  }
  
  .store-address p {
    font-size: 0.9rem;
  }
  
  .detail-row {
    font-size: 0.8rem;
  }
  
  .detail-label {
    min-width: 60px;
  }
}

/* 小屏幕手机端使用垂直布局 */
@media (max-width: 480px) {
  .stores-section {
    padding: 2rem 0;
  }
  
  .stores-section::before {
    width: 15%;
    opacity: 0.03;
  }
  
  .stores-main-content {
    display: flex;
    flex-direction: row;
    gap: var(--space-md);
    align-items: flex-start;
    grid-template-columns: none;
  }
  
  .stores-left {
    flex: 1;
    width: auto;
  }
  
  .stores-right {
    flex: 0 0 20%;
    height: auto;
    min-width: 80px;
  }
  
  .stores-summary {
    height: auto !important;
  }
  
  .summary-stats {
    flex: none !important;
    justify-content: flex-start !important;
    gap: 0.6rem !important;
    padding: 0.8rem !important;
    min-height: auto !important;
  }
  
  .stores-slider {
    width: 300%; /* Keep horizontal scroll on mobile */
  }
  
  .store-feature {
    display: flex;
    flex-direction: column;
    gap: var(--space-md);
    padding: var(--space-sm);
    min-height: auto;
    width: 80%;
    max-width: 80%;
    box-sizing: border-box;
    overflow: hidden;
    grid-template-columns: none;
    align-items: stretch;
  }
  
  .store-feature.reverse {
    display: flex;
    flex-direction: column;
    direction: ltr;
  }
  
  .store-feature.reverse > * {
    direction: ltr;
  }
  
  .store-image-container {
    position: relative;
    width: 100%;
    max-width: 100%;
    flex: 0 0 auto;
    box-sizing: border-box;
    overflow: hidden;
    border-radius: var(--radius-md);
    background: transparent;
    display: block;
    align-items: normal;
    justify-content: normal;
  }
  
  .store-image-container::before {
    display: none;
  }
  
  .store-image {
    height: 200px;
    width: 100%;
    max-width: 100%;
    border-radius: var(--radius-md);
    object-fit: cover;
    display: block;
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    position: relative;
    z-index: 2;
  }
  
  .store-content {
    width: 100%;
    max-width: 100%;
    flex: 1;
    padding: 1.2rem;
    border-radius: var(--radius-sm);
    box-sizing: border-box;
    overflow: hidden;
    background: var(--gradient-card);
    border: 1px solid rgba(30, 64, 175, 0.1);
    backdrop-filter: none;
    transform: none;
    transition: none;
  }
  
  .store-content:hover {
    transform: none;
  }
  
  .store-title {
    font-size: 1.3rem;
    margin-bottom: 0.8rem;
    word-wrap: break-word;
    overflow-wrap: break-word;
  }
  
  .store-location {
    margin-bottom: 0.8rem;
  }
  
  .city-name {
    font-size: 0.9rem;
  }
  
  .store-address {
    margin-bottom: 1rem;
  }
  
  .store-address p {
    font-size: 0.9rem;
    word-wrap: break-word;
  }
  
  .store-features {
    gap: 0.6rem;
    margin-bottom: 1.2rem;
    flex-wrap: wrap;
  }
  
  .feature-tag {
    font-size: 0.8rem;
    padding: 0.3rem 0.6rem;
    white-space: nowrap;
  }
  
  .store-details {
    margin-bottom: 1.2rem;
  }
  
  .detail-row {
    font-size: 0.85rem;
    margin-bottom: 0.4rem;
    word-wrap: break-word;
  }
  
  .detail-label {
    min-width: 60px;
    flex-shrink: 0;
  }
  
  .detail-value {
    flex: 1;
    word-wrap: break-word;
  }
  
  .action-btn {
    padding: 0.7rem 1rem;
    font-size: 0.85rem;
    width: 100%;
    box-sizing: border-box;
    white-space: nowrap;
  }
  
  .store-actions {
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
    width: 100%;
  }
  
  .stores-summary {
    border-radius: 12px;
  }
  
  .summary-header {
    padding: 1rem 1rem 0.8rem;
  }
  
  .summary-title {
    font-size: 1.2rem;
  }
  
  .summary-subtitle {
    font-size: 0.8rem;
  }
  
  .summary-stats {
    padding: 1rem;
    min-height: 200px;
    gap: 0.6rem;
    background: transparent;
  }
  
  .stat-item {
    padding: var(--space-sm) var(--space-xs);
    background: var(--gradient-card);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08), 0 1px 5px rgba(30, 64, 175, 0.04);
    border: 1px solid rgba(30, 64, 175, 0.1);
    border-radius: var(--radius-sm);
  }
  
  .stat-number {
    font-size: 1.8rem;
    letter-spacing: -0.5px;
    margin-bottom: 0.2rem;
  }
  
  .stat-label {
    font-size: 0.7rem;
    line-height: 1.1;
  }
  
  .stores-navigation {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: var(--space-md);
    margin-top: var(--space-lg);
    padding: var(--space-md);
    border-top: 1px solid var(--gray-200);
    width: 80%;
    margin-left: 0;
    margin-right: 0;
    box-sizing: border-box;
  }
  
  .stores-navigation .nav-dots {
    order: -1;
    display: flex;
    gap: 0.6rem;
  }
  
  .stores-navigation .nav-dot {
    width: 10px;
    height: 10px;
  }
  
  .stores-navigation .nav-counter {
    font-size: 0.9rem;
  }
  
  .stores-navigation .nav-btn {
    width: 40px;
    height: 40px;
  }
}



/* About Section - Split Layout */
.about-section {
  background: linear-gradient(180deg, #334155 0%, #1e293b 50%, #1a1a2e 100%);
  padding: 4rem 0;
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
}

.about-section .container {
  width: 100%;
}

.about-section .section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.about-section .section-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 1.5rem;
  letter-spacing: 2px;
}

.about-section .section-subtitle {
  font-size: 1.3rem;
  color: rgba(255, 255, 255, 0.7);
  font-weight: 400;
  letter-spacing: 1px;
  line-height: 1.6;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: 1fr;
  gap: 1.5rem;
  max-width: 1200px;
  margin: 0 auto;
  height: 500px;
}

.about-panel {
  position: relative;
  overflow: hidden;
  cursor: pointer;
  transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.panel-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.panel-content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  color: white;
  text-align: center;
  transition: all 0.6s ease;
}

.panel-header {
  transition: all 0.6s ease;
}

.panel-category {
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  opacity: 0.8;
  margin-bottom: 1rem;
  display: block;
}

.panel-title {
  font-size: 2.8rem;
  font-weight: 900;
  margin-bottom: 1.5rem;
  line-height: 1.1;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}

.panel-details {
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.6s ease;
  max-width: 90%;
}

.panel-description {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  font-weight: 300;
}

.about-panel:hover .panel-details {
  opacity: 1;
  transform: translateY(0);
}

.about-panel:hover .panel-header {
  transform: translateY(-20px);
}

/* Heritage Panel */
.heritage-panel {
  background: linear-gradient(135deg, #1e40af 0%, #1d4ed8 100%);
}

.heritage-illustration {
  position: relative;
  width: 100%;
  height: 100%;
}

.mountain-silhouette {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 40%;
  background: linear-gradient(to top, #1e3a8a 0%, transparent 100%);
  clip-path: polygon(0 100%, 15% 70%, 35% 85%, 55% 60%, 75% 75%, 100% 50%, 100% 100%);
}

.tea-leaves {
  position: absolute;
  width: 15px;
  height: 22px;
  background: #10b981;
  border-radius: 50% 0 50% 50%;
  animation: float 4s ease-in-out infinite;
}

.floating-1 {
  top: 20%;
  left: 15%;
  animation-delay: 0s;
}

.floating-2 {
  top: 60%;
  right: 20%;
  animation-delay: 1s;
}

.floating-3 {
  top: 35%;
  left: 70%;
  animation-delay: 2s;
}

.sunrise-circle {
  position: absolute;
  top: 15%;
  right: 15%;
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, #fbbf24 0%, #f59e0b 100%);
  border-radius: 50%;
  opacity: 0.8;
  box-shadow: 0 0 40px rgba(251, 191, 36, 0.4);
}

/* Culture Panel */
.culture-panel {
  background: linear-gradient(135deg, #1e3a8a 0%, #1e40af 100%);
}

.culture-illustration {
  position: relative;
  width: 100%;
  height: 100%;
}

.panda-shape {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90px;
  height: 90px;
  background: #ffffff;
  border-radius: 50%;
  box-shadow: 
    -15px -15px 0 #000 inset,
    15px -15px 0 #000 inset,
    0 30px 0 #000 inset;
}

.bamboo-1, .bamboo-2 {
  position: absolute;
  width: 6px;
  background: linear-gradient(to bottom, #10b981 0%, #059669 100%);
  border-radius: 3px;
}

.bamboo-1 {
  height: 50%;
  top: 15%;
  left: 25%;
}

.bamboo-2 {
  height: 40%;
  top: 30%;
  right: 30%;
}

.culture-dots {
  position: absolute;
  width: 12px;
  height: 12px;
  background: #60a5fa;
  border-radius: 50%;
  animation: pulse 2s ease-in-out infinite;
}

.dot-1 { top: 25%; left: 35%; }
.dot-2 { top: 65%; right: 30%; animation-delay: 0.5s; }
.dot-3 { bottom: 20%; left: 25%; animation-delay: 1s; }

/* Quality Panel */
.quality-panel {
  background: linear-gradient(135deg, #0f4c75 0%, #1e40af 100%);
}

.quality-illustration {
  position: relative;
  width: 100%;
  height: 100%;
}

.tea-cup {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 60px;
  height: 45px;
  background: linear-gradient(to bottom, #f3f4f6 0%, #e5e7eb 100%);
  border-radius: 0 0 30px 30px;
  border: 2px solid #374151;
}

.tea-cup::before {
  content: '';
  position: absolute;
  top: -8px;
  left: 50%;
  transform: translateX(-50%);
  width: 50px;
  height: 15px;
  background: #10b981;
  border-radius: 50%;
}

.steam-lines {
  position: absolute;
  width: 2px;
  height: 30px;
  background: rgba(255, 255, 255, 0.6);
  border-radius: 2px;
  animation: steam 2s ease-in-out infinite;
}

.line-1 { top: 20%; left: 45%; }
.line-2 { top: 25%; left: 50%; animation-delay: 0.3s; }
.line-3 { top: 20%; left: 55%; animation-delay: 0.6s; }

.quality-star {
  position: absolute;
  width: 0;
  height: 0;
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-bottom: 5px solid #fbbf24;
  animation: twinkle 3s ease-in-out infinite;
}

.star-1 { top: 20%; right: 20%; }
.star-2 { top: 70%; left: 15%; animation-delay: 1s; }
.star-3 { bottom: 25%; right: 30%; animation-delay: 2s; }

/* Mission Panel */
.mission-panel {
  background: linear-gradient(135deg, #1e3a8a 0%, #0f172a 100%);
}

.mission-illustration {
  position: relative;
  width: 100%;
  height: 100%;
}

.heart-shape {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 45px;
  height: 40px;
  background: #3b82f6;
}

.heart-shape::before,
.heart-shape::after {
  content: '';
  position: absolute;
  left: 22px;
  top: 0;
  width: 22px;
  height: 36px;
  background: #3b82f6;
  border-radius: 22px 22px 0 0;
  transform: rotate(-45deg);
  transform-origin: 0 100%;
}

.heart-shape::after {
  left: 0;
  transform: rotate(45deg);
  transform-origin: 100% 100%;
}

.mission-waves {
  position: absolute;
  width: 150px;
  height: 150px;
  border: 2px solid rgba(96, 165, 250, 0.3);
  border-radius: 50%;
  animation: ripple 4s ease-out infinite;
}

.wave-1 { top: 50%; left: 50%; transform: translate(-50%, -50%); }
.wave-2 { top: 50%; left: 50%; transform: translate(-50%, -50%); animation-delay: 1s; }
.wave-3 { top: 50%; left: 50%; transform: translate(-50%, -50%); animation-delay: 2s; }

.mission-particles {
  position: absolute;
  width: 5px;
  height: 5px;
  background: #fbbf24;
  border-radius: 50%;
  animation: float 3s ease-in-out infinite;
}

.particle-1 { top: 30%; left: 30%; }
.particle-2 { top: 70%; right: 35%; animation-delay: 1s; }
.particle-3 { bottom: 30%; left: 60%; animation-delay: 2s; }

/* Panel Content Styles */
.panel-stats {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.stat-item {
  text-align: center;
  flex: 1;
  min-width: 0;
  max-width: 120px;
}

.stat-number {
  font-size: 1.6rem;
  font-weight: 900;
  color: #fbbf24;
  display: block;
  margin-bottom: 0.4rem;
  line-height: 1.1;
}

.stat-label {
  font-size: 0.8rem;
  opacity: 0.8;
  word-wrap: break-word;
  line-height: 1.2;
}

.panel-features {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  justify-content: center;
  margin-top: 1.5rem;
}

.feature-tag {
  background: rgba(255, 255, 255, 0.2);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
}

.quality-metrics {
  margin-top: 1.5rem;
}

.metric-item {
  text-align: center;
}

.metric-number {
  font-size: 2.5rem;
  font-weight: 900;
  color: #fbbf24;
  display: block;
  margin-bottom: 0.5rem;
}

.metric-label {
  font-size: 1rem;
  opacity: 0.9;
}

.mission-quote {
  font-size: 1.8rem;
  font-weight: 700;
  font-style: italic;
  margin-bottom: 1.5rem;
  color: #fbbf24;
  line-height: 1.3;
}

.mission-values {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 1.5rem;
}

.value-item {
  background: rgba(255, 255, 255, 0.2);
  padding: 0.6rem 1.2rem;
  border-radius: 25px;
  font-weight: 600;
  font-size: 0.85rem;
}

/* Animations */
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes pulse {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.2); opacity: 0.7; }
}

@keyframes steam {
  0% { opacity: 0; transform: translateY(0); }
  50% { opacity: 1; }
  100% { opacity: 0; transform: translateY(-20px); }
}

@keyframes twinkle {
  0%, 100% { opacity: 0.5; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); }
}

@keyframes ripple {
  0% { transform: translate(-50%, -50%) scale(0); opacity: 1; }
  100% { transform: translate(-50%, -50%) scale(2); opacity: 0; }
}



/* About Section Responsive */
@media (max-width: 1024px) {
  .about-section {
    min-height: auto;
    align-items: flex-start;
    padding: 3rem 0;
  }
  
  .about-section .section-header {
    margin-bottom: 2.5rem;
  }
  
  .about-section .section-title {
    font-size: 3rem;
  }
  
  .about-section .section-subtitle {
    font-size: 1.2rem;
  }
  
  .about-grid {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    max-width: 900px;
    height: 600px;
    gap: 1.5rem;
  }
  
  .panel-content {
    padding: 2.5rem;
  }
  
  .panel-title {
    font-size: 3rem;
  }
}

@media (max-width: 768px) {
  .about-section {
    min-height: auto;
    align-items: flex-start;
    padding: 3rem 0;
  }
  
  .about-section .section-header {
    margin-bottom: 2rem;
  }
  
  .about-section .section-title {
    font-size: 2.5rem;
  }
  
  .about-section .section-subtitle {
    font-size: 1.1rem;
  }
  
  .about-grid {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, 1fr);
    max-width: 600px;
    height: 800px;
    gap: 1rem;
  }
  
  .panel-content {
    padding: 2rem;
  }
  
  .panel-title {
    font-size: 2.5rem;
  }
  
  .panel-description {
    font-size: 1rem;
  }
  
  .panel-stats {
    gap: 0.8rem;
  }
  
  .stat-item {
    max-width: 100px;
  }
  
  .stat-number {
    font-size: 1.4rem;
  }
  
  .mission-quote {
    font-size: 1.6rem;
  }
  
  .mission-values {
    flex-direction: column;
    gap: 0.8rem;
  }
  
  .panel-features {
    gap: 0.6rem;
  }
  
  .feature-tag {
    font-size: 0.7rem;
    padding: 0.4rem 0.8rem;
  }
}

@media (max-width: 480px) {
  .about-section {
    min-height: auto;
    align-items: flex-start;
    padding: 2rem 0;
  }
  
  .about-section .section-header {
    margin-bottom: 1.5rem;
  }
  
  .about-section .section-title {
    font-size: 2rem;
  }
  
  .about-section .section-subtitle {
    font-size: 1rem;
  }
  
  .about-grid {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, 1fr);
    max-width: 100%;
    height: 600px;
    gap: 0.8rem;
  }
  
  .panel-content {
    padding: 1.5rem;
  }
  
  .panel-category {
    font-size: 0.6rem;
    letter-spacing: 2px;
  }
  
  .panel-title {
    font-size: 2rem;
    margin-bottom: 1rem;
  }
  
  .panel-description {
    font-size: 0.9rem;
    margin-bottom: 1rem;
  }
  
  .panel-stats {
    flex-direction: row;
    gap: 0.6rem;
    justify-content: center;
  }
  
  .stat-item {
    max-width: 80px;
  }
  
  .stat-number {
    font-size: 1.2rem;
  }
  
  .stat-label {
    font-size: 0.7rem;
  }
  
  .mission-quote {
    font-size: 1.4rem;
    margin-bottom: 1rem;
  }
  
  .mission-values {
    flex-direction: column;
    gap: 0.6rem;
  }
  
  .value-item {
    padding: 0.6rem 1rem;
    font-size: 0.9rem;
  }
  
  .panel-features {
    gap: 0.5rem;
  }
  
  .feature-tag {
    font-size: 0.6rem;
    padding: 0.3rem 0.6rem;
  }
  
  .metric-number {
    font-size: 2rem;
  }
  
  .metric-label {
    font-size: 0.9rem;
  }
  
  /* Reduce animation elements size on mobile */
  .panda-shape {
    width: 80px;
    height: 80px;
  }
  
  .tea-cup {
    width: 60px;
    height: 45px;
  }
  
  .sunrise-circle {
    width: 60px;
    height: 60px;
  }
  
  .heart-shape {
    width: 40px;
    height: 36px;
  }
}

/* 性能优化和动画支持 */
.product-image-container,
.store-image-container,
.about-panel {
  transform-style: preserve-3d;
  backface-visibility: hidden;
  transform-origin: center center;
}

.products-slider,
.stores-slider,
.hero-tags,
.title-line-1,
.title-line-2,
.hero-description,
.hero-cta,
.hero-subtitle,
.section-title,
.product-slide,
.store-slide,
.stat-number,
.nav-dot,
.nav-counter {
  will-change: transform, opacity;
}

/* 按钮通用样式 */
.cta-button,
.hero-cta,
.action-btn {
  transform-origin: center center;
  transition: all 0.3s ease;
}

.cta-button:hover,
.hero-cta:hover,
.action-btn:hover {
  box-shadow: 
    0 8px 25px rgba(30, 64, 175, 0.25),
    0 4px 10px rgba(0, 0, 0, 0.1);
}

html {
  scroll-behavior: smooth;
}

/* 装饰性背景 */
.main-content::before {
  content: '';
  position: absolute;
  inset: 0;
  background: 
    radial-gradient(circle at 20% 50%, rgba(30, 64, 175, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(59, 130, 246, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 40% 80%, rgba(30, 64, 175, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}
</style>


