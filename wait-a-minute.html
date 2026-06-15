<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>等一下 · 冲动拦截器</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC", "Microsoft YaHei", sans-serif;
    background: #ffffff;
    color: #333;
    min-height: 100vh;
    display: flex;
    justify-content: center;
  }

  .app-container {
    width: 100%;
    max-width: 420px;
    min-height: 100vh;
    position: relative;
    overflow: hidden;
  }

  .page {
    display: none;
    flex-direction: column;
    min-height: 100vh;
    padding: 24px 20px;
  }

  .page.active { display: flex; }

  /* ── 页面1：启动页 ── */
  .page1 {
    align-items: center;
    justify-content: center;
    padding-top: 80px;
  }

  .page1 .icon {
    font-size: 64px;
    color: #FF8C42;
    margin-bottom: 24px;
    line-height: 1;
  }

  .page1 .title {
    font-size: 28px;
    font-weight: bold;
    color: #1a3c5e;
    text-align: center;
    margin-bottom: 12px;
    line-height: 1.3;
  }

  .page1 .subtitle {
    font-size: 16px;
    color: #999;
    text-align: center;
    margin-bottom: 48px;
  }

  .btn-start {
    display: inline-block;
    background: #2E8B9E;
    color: #fff;
    font-size: 18px;
    font-weight: 600;
    padding: 14px 0;
    width: 200px;
    text-align: center;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    transition: background 0.2s;
  }

  .btn-start:hover { background: #257a8c; }
  .btn-start:active { background: #1e6b7a; }

  /* ── 页面2：商品信息输入页 ── */
  .page2 .section-title {
    font-size: 20px;
    font-weight: 600;
    color: #333;
    text-align: left;
    margin-bottom: 24px;
  }

  .input-group {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 20px;
  }

  .input-field {
    width: 100%;
    padding: 16px;
    font-size: 16px;
    background: #f5f5f5;
    border: 2px solid transparent;
    border-radius: 12px;
    outline: none;
    transition: border-color 0.2s;
  }

  .input-field:focus { border-color: #2E8B9E; background: #fff; }

  .examples-label {
    font-size: 13px;
    color: #999;
    margin-bottom: 12px;
  }

  .examples-row {
    display: flex;
    gap: 10px;
    margin-bottom: 32px;
  }

  .example-btn {
    flex: 1;
    background: #f0f4f5;
    border: 1.5px solid #e0e0e0;
    border-radius: 20px;
    padding: 12px 8px;
    font-size: 13px;
    color: #555;
    cursor: pointer;
    text-align: center;
    transition: all 0.15s;
    white-space: nowrap;
  }

  .example-btn:hover { background: #e3f0f2; border-color: #2E8B9E; }
  .example-btn:active { background: #d4eaee; }

  .btn-analyze {
    display: block;
    width: 100%;
    background: #DECE59;
    color: #333;
    font-size: 17px;
    font-weight: 600;
    padding: 16px 0;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    margin-top: auto;
    transition: background 0.2s;
  }

  .btn-analyze:hover { background: #d4c43e; }
  .btn-analyze:active { background: #c9b92e; }

  .toast {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    background: #e74c3c;
    color: #fff;
    padding: 12px 24px;
    border-radius: 12px;
    font-size: 14px;
    z-index: 999;
    opacity: 0;
    transition: opacity 0.3s;
    pointer-events: none;
  }

  .toast.show { opacity: 1; }

  /* ── 页面3/4/5：AI提问页 ── */
  .chat-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 16px;
  }

  .chat-avatar {
    width: 44px;
    height: 44px;
    border-radius: 50%;
    background: #e8f4f6;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    flex-shrink: 0;
  }

  .chat-name {
    font-size: 15px;
    font-weight: 600;
    color: #555;
  }

  .chat-bubble {
    background: #f5f7f8;
    border-radius: 18px;
    border-top-left-radius: 4px;
    padding: 18px 20px;
    font-size: 16px;
    color: #333;
    line-height: 1.6;
    margin-bottom: 28px;
    max-width: 100%;
  }

  .options-container {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .options-row {
    display: flex;
    gap: 12px;
  }

  .options-row .option-btn { flex: 1; }

  .option-btn {
    display: block;
    width: 100%;
    background: #f0f4f5;
    border: 2px solid #e8e8e8;
    border-radius: 14px;
    padding: 16px 20px;
    font-size: 16px;
    color: #444;
    cursor: pointer;
    text-align: center;
    transition: all 0.15s;
  }

  .option-btn:hover { background: #e3f0f2; border-color: #2E8B9E; }
  .option-btn:active { background: #d4eaee; }

  /* ── 页面5 机会成本展示 ── */
  .cost-breakdown {
    background: #fffbf0;
    border: 1.5px solid #DECE59;
    border-radius: 12px;
    padding: 14px 18px;
    margin-bottom: 20px;
    font-size: 14px;
    color: #8a7b2a;
    text-align: center;
    line-height: 1.6;
  }

  .cost-breakdown strong { color: #c9a800; }

  /* ── 页面6：分析报告页 ── */
  .report-title {
    font-size: 18px;
    font-weight: bold;
    color: #1a3c5e;
    text-align: center;
    margin-bottom: 20px;
    line-height: 1.4;
  }

  .product-info-row {
    background: #f5f5f5;
    border-radius: 8px;
    padding: 12px 16px;
    font-size: 15px;
    color: #555;
    margin-bottom: 20px;
    text-align: center;
  }

  .analysis-cards {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 20px;
  }

  .analysis-card {
    background: #fafafa;
    border-radius: 12px;
    padding: 16px 18px;
    border: 1px solid #eee;
  }

  .analysis-card .card-label {
    font-size: 13px;
    color: #999;
    margin-bottom: 6px;
  }

  .analysis-card .card-answer {
    font-size: 15px;
    color: #444;
    margin-bottom: 4px;
  }

  .analysis-card .card-judgment {
    font-size: 14px;
    font-weight: 600;
    color: #2E8B9E;
  }

  .advice-box {
    background: #fff8f0;
    border: 1.5px solid #FF8C42;
    border-radius: 14px;
    padding: 18px 20px;
    margin-bottom: 16px;
    text-align: center;
  }

  .advice-box .advice-verdict {
    font-size: 28px;
    margin-bottom: 8px;
  }

  .advice-box .advice-reason {
    font-size: 14px;
    color: #8a6a3a;
    line-height: 1.5;
  }

  .summary-text {
    text-align: center;
    font-size: 15px;
    color: #666;
    margin-bottom: 28px;
    line-height: 1.5;
  }

  .report-actions {
    display: flex;
    gap: 12px;
  }

  .report-actions .btn-action {
    flex: 1;
    padding: 14px 0;
    font-size: 15px;
    font-weight: 600;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    text-align: center;
    transition: background 0.2s;
  }

  .btn-restart {
    background: #f0f0f0;
    color: #555;
  }

  .btn-restart:hover { background: #e4e4e4; }
  .btn-restart:active { background: #d8d8d8; }

  .btn-download {
    background: #2E8B9E;
    color: #fff;
  }

  .btn-download:hover { background: #257a8c; }
  .btn-download:active { background: #1e6b7a; }
</style>
</head>
<body>

<div class="app-container">

  <!-- ═══ 页面1：启动页 ═══ -->
  <div class="page page1 active" id="page1">
    <div class="icon">⏸️</div>
    <h1 class="title">等一下 · 冲动拦截器<br>（Wait a minute）</h1>
    <p class="subtitle">购物前，让AI问你3个问题</p>
    <button class="btn-start" onclick="goTo('page2')">开始拦截</button>
  </div>

  <!-- ═══ 页面2：商品信息输入页 ═══ -->
  <div class="page page2" id="page2">
    <h2 class="section-title">📦 把你想买的商品告诉我</h2>

    <div class="input-group">
      <input class="input-field" id="productName" type="text" placeholder="商品名称，如：耐克运动鞋" autocomplete="off">
      <input class="input-field" id="productPrice" type="number" placeholder="价格，如：500" min="0" step="0.01" autocomplete="off">
    </div>

    <p class="examples-label">或者试试这些例子（点击自动填入）：</p>
    <div class="examples-row">
      <button class="example-btn" onclick="fillExample('运动鞋', 500)">👟 运动鞋 / 500元</button>
      <button class="example-btn" onclick="fillExample('平板电脑', 3999)">📱 平板电脑 / 3999元</button>
      <button class="example-btn" onclick="fillExample('面霜', 298)">💄 面霜 / 298元</button>
    </div>

    <button class="btn-analyze" onclick="startAnalyze()">冷静一下，开始分析</button>
  </div>

  <!-- ═══ 页面3：问题1 ═══ -->
  <div class="page page3" id="page3">
    <div class="chat-header">
      <div class="chat-avatar">🤖</div>
      <span class="chat-name">等一下助手</span>
    </div>
    <div class="chat-bubble">
      如果这件商品完全没有折扣，你还会买吗？还是说，只是觉得不买就亏了？
    </div>
    <div class="options-row">
      <button class="option-btn" onclick="answerQ1('还是会买')">✅ 还是会买</button>
      <button class="option-btn" onclick="answerQ1('主要是怕错过折扣')">❌ 主要是怕错过折扣</button>
    </div>
  </div>

  <!-- ═══ 页面4：问题2 ═══ -->
  <div class="page page4" id="page4">
    <div class="chat-header">
      <div class="chat-avatar">🤖</div>
      <span class="chat-name">等一下助手</span>
    </div>
    <div class="chat-bubble">
      你过去30天买过类似的商品吗？上次买的那个，你用过几次？
    </div>
    <div class="options-container">
      <button class="option-btn" onclick="answerQ2('买过，很少用')">买过，很少用</button>
      <button class="option-btn" onclick="answerQ2('买过，经常用')">买过，经常用</button>
      <button class="option-btn" onclick="answerQ2('没买过')">没买过</button>
    </div>
  </div>

  <!-- ═══ 页面5：问题3 ═══ -->
  <div class="page page5" id="page5">
    <div class="chat-header">
      <div class="chat-avatar">🤖</div>
      <span class="chat-name">等一下助手</span>
    </div>

    <div class="cost-breakdown" id="costBreakdown"></div>

    <div class="chat-bubble" id="q3Bubble"></div>
    <div class="options-row">
      <button class="option-btn" onclick="answerQ3('更想要体验')">🍲 更想要体验</button>
      <button class="option-btn" onclick="answerQ3('还是想要商品')">👟 还是想要商品</button>
    </div>
  </div>

  <!-- ═══ 页面6：分析报告页 ═══ -->
  <div class="page page6" id="page6">
    <h2 class="report-title">【等一下 · 冷静分析报告】</h2>
    <div class="product-info-row" id="reportProductInfo"></div>

    <div class="analysis-cards" id="analysisCards"></div>

    <div class="advice-box" id="adviceBox"></div>
    <div class="summary-text" id="summaryText"></div>

    <div class="report-actions">
      <button class="btn-action btn-restart" onclick="restart()">🔁 重新分析</button>
      <button class="btn-action btn-download" onclick="downloadReport()">📥 下载报告</button>
    </div>
  </div>

</div>

<div class="toast" id="toast"></div>

<script>
// ═══════════════════════════════════════════
// 全局数据存储
// ═══════════════════════════════════════════
var Store = {
  productName: '',
  productPrice: 0,
  q1: '',  // 问题1答案
  q2: '',  // 问题2答案
  q3: ''   // 问题3答案
};

// ═══════════════════════════════════════════
// 工具函数
// ═══════════════════════════════════════════

function goTo(pageId) {
  document.querySelectorAll('.page').forEach(function(p) {
    p.classList.remove('active');
  });
  document.getElementById(pageId).classList.add('active');
  // 滚动到顶部
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function showToast(msg) {
  var toast = document.getElementById('toast');
  toast.textContent = msg;
  toast.classList.add('show');
  clearTimeout(toast._timeout);
  toast._timeout = setTimeout(function() {
    toast.classList.remove('show');
  }, 2000);
}

function resetStore() {
  Store.productName = '';
  Store.productPrice = 0;
  Store.q1 = '';
  Store.q2 = '';
  Store.q3 = '';
}

// ═══════════════════════════════════════════
// 页面2：填充示例 & 开始分析
// ═══════════════════════════════════════════

function fillExample(name, price) {
  document.getElementById('productName').value = name;
  document.getElementById('productPrice').value = price;
}

function startAnalyze() {
  var nameInput = document.getElementById('productName');
  var priceInput = document.getElementById('productPrice');
  var name = nameInput.value.trim();
  var priceStr = priceInput.value.trim();

  if (!name || !priceStr) {
    showToast('请填写商品名称和价格');
    return;
  }

  var price = parseFloat(priceStr);
  if (isNaN(price) || price <= 0) {
    showToast('请输入有效的价格');
    return;
  }

  Store.productName = name;
  Store.productPrice = price;

  goTo('page3');
}

// ═══════════════════════════════════════════
// 页面3：问题1
// ═══════════════════════════════════════════

function answerQ1(answer) {
  Store.q1 = answer;
  goTo('page4');
}

// ═══════════════════════════════════════════
// 页面4：问题2
// ═══════════════════════════════════════════

function answerQ2(answer) {
  Store.q2 = answer;
  // 进入页面5前，先计算并渲染机会成本
  renderOpportunityCost();
  goTo('page5');
}

// ═══════════════════════════════════════════
// 页面5：问题3 — 机会成本换算
// ═══════════════════════════════════════════

function renderOpportunityCost() {
  var price = Store.productPrice;
  var meals = Math.floor(price / 50);
  var massages = Math.floor(price / 100);
  var teas = Math.floor(price / 25);

  var breakdownEl = document.getElementById('costBreakdown');
  breakdownEl.innerHTML = '💡 <strong>' + price + '元</strong> ≈ <strong>' + meals + '顿饭</strong> / <strong>' + massages + '次按摩</strong> / <strong>' + teas + '杯奶茶</strong>';

  var bubbleEl = document.getElementById('q3Bubble');
  bubbleEl.textContent = '这' + price + '元，换成你最爱的' + meals + '顿饭 / ' + massages + '次按摩 / ' + teas + '杯奶茶。你更想要商品，还是这些体验？';
}

function answerQ3(answer) {
  Store.q3 = answer;
  renderReport();
  goTo('page6');
}

// ═══════════════════════════════════════════
// 页面6：分析报告 — 动态生成
// ═══════════════════════════════════════════

function renderReport() {
  var price = Store.productPrice;
  var meals = Math.floor(price / 50);
  var massages = Math.floor(price / 100);
  var teas = Math.floor(price / 25);

  // 商品信息行
  document.getElementById('reportProductInfo').textContent =
    '商品：' + Store.productName + '，价格：' + price + '元';

  // ── 分析卡片 ──
  var cardsHtml = '';

  // 卡片1：折扣幻觉
  var card1Answer, card1Judgment;
  if (Store.q1 === '主要是怕错过折扣') {
    card1Answer = '你主要是怕错过折扣';
    card1Judgment = '→ 判断：不是真实需求';
  } else {
    card1Answer = '你是真实需要';
    card1Judgment = '→ 判断：可以再想想是否需要';
  }
  cardsHtml += '' +
    '<div class="analysis-card">' +
      '<div class="card-label">折扣幻觉？</div>' +
      '<div class="card-answer">' + card1Answer + '</div>' +
      '<div class="card-judgment">' + card1Judgment + '</div>' +
    '</div>';

  // 卡片2：同类存货
  var card2Answer, card2Judgment;
  if (Store.q2 === '买过，很少用') {
    card2Answer = '你买过类似但很少用';
    card2Judgment = '→ 判断：边际效用低';
  } else if (Store.q2 === '买过，经常用') {
    card2Answer = '你经常用这类商品';
    card2Judgment = '→ 判断：确实是高频需求';
  } else {
    card2Answer = '你没买过类似的';
    card2Judgment = '→ 判断：可能是新尝试';
  }
  cardsHtml += '' +
    '<div class="analysis-card">' +
      '<div class="card-label">同类存货？</div>' +
      '<div class="card-answer">' + card2Answer + '</div>' +
      '<div class="card-judgment">' + card2Judgment + '</div>' +
    '</div>';

  // 卡片3：机会成本换算
  var card3Answer = price + '元 = ' + meals + '顿饭 / ' + massages + '次按摩 / ' + teas + '杯奶茶';
  var card3Judgment;
  if (Store.q3 === '更想要体验') {
    card3Judgment = '→ 判断：商品性价比不高';
  } else {
    card3Judgment = '→ 判断：商品对你确有价值';
  }
  cardsHtml += '' +
    '<div class="analysis-card">' +
      '<div class="card-label">机会成本换算</div>' +
      '<div class="card-answer">' + card3Answer + '</div>' +
      '<div class="card-judgment">' + card3Judgment + '</div>' +
    '</div>';

  document.getElementById('analysisCards').innerHTML = cardsHtml;

  // ── 计分逻辑 ──
  // 偏向"不买"的得分点
  var scoreNoBuy = 0;
  var scoreBuy = 0;

  if (Store.q1 === '主要是怕错过折扣') scoreNoBuy++;
  else scoreBuy++;

  if (Store.q2 === '买过，很少用') scoreNoBuy++;
  else if (Store.q2 === '买过，经常用') scoreBuy++;
  // "没买过" → 中性，不加任何一方

  if (Store.q3 === '更想要体验') scoreNoBuy++;
  else scoreBuy++;

  // ── 建议框 ──
  var verdict = '';
  var reason = '';
  var summary = '';

  if (scoreNoBuy >= 2) {
    verdict = '❌ 不买';
    reason = '折扣可能只是营销手段，同类商品你买过但使用率不高，而且这些钱换成的体验对你更有吸引力——综合来看，这件商品不是必需品。';
    summary = '💬 省下的' + price + '元，换成' + meals + '顿饭 / ' + massages + '次按摩 / ' + teas + '杯奶茶可能更快乐';
  } else if (scoreBuy >= 2) {
    verdict = '✅ 买';
    reason = '你是真实需要这件商品，同类商品你也经常使用，而且你确认商品比体验更有价值。';
    summary = '💬 你买的是功能与情绪价值，确认值得就行';
  } else {
    verdict = '⏳ 等3天再决定';
    reason = '你的判断有些摇摆——不急这一时，给自己三天冷静期，冲动会自然消退。';
    summary = '💬 放3天再看，冲动会下降一半';
  }

  document.getElementById('adviceBox').innerHTML = '' +
    '<div class="advice-verdict">' + verdict + '</div>' +
    '<div class="advice-reason">' + reason + '</div>';

  document.getElementById('summaryText').textContent = summary;

  // 保存报告数据供下载使用
  Store.report = {
    card1Answer: card1Answer,
    card1Judgment: card1Judgment,
    card2Answer: card2Answer,
    card2Judgment: card2Judgment,
    card3Answer: card3Answer,
    card3Judgment: card3Judgment,
    verdict: verdict,
    reason: reason,
    summary: summary,
    meals: meals,
    massages: massages,
    teas: teas
  };
}

// ═══════════════════════════════════════════
// 底部按钮操作
// ═══════════════════════════════════════════

function restart() {
  resetStore();
  document.getElementById('productName').value = '';
  document.getElementById('productPrice').value = '';
  goTo('page2');
}

function downloadReport() {
  var r = Store.report;
  var price = Store.productPrice;

  var now = new Date();
  var dateStr = now.getFullYear() + '-' +
    String(now.getMonth() + 1).padStart(2, '0') + '-' +
    String(now.getDate()).padStart(2, '0') + ' ' +
    String(now.getHours()).padStart(2, '0') + ':' +
    String(now.getMinutes()).padStart(2, '0') + ':' +
    String(now.getSeconds()).padStart(2, '0');

  var content = '';
  content += '══════════════════════════════════\n';
  content += '  【等一下 · 冷静分析报告】\n';
  content += '══════════════════════════════════\n\n';
  content += '商品名称：' + Store.productName + '\n';
  content += '价格：' + price + ' 元\n\n';
  content += '──────────────────────────────\n';
  content += '  分析卡片\n';
  content += '──────────────────────────────\n\n';
  content += '【折扣幻觉？】\n';
  content += '  你的回答：' + r.card1Answer + '\n';
  content += '  判断：' + r.card1Judgment.replace('→ 判断：', '') + '\n\n';
  content += '【同类存货？】\n';
  content += '  你的回答：' + r.card2Answer + '\n';
  content += '  判断：' + r.card2Judgment.replace('→ 判断：', '') + '\n\n';
  content += '【机会成本换算】\n';
  content += '  ' + r.card3Answer + '\n';
  content += '  判断：' + r.card3Judgment.replace('→ 判断：', '') + '\n\n';
  content += '──────────────────────────────\n';
  content += '  拦截建议\n';
  content += '──────────────────────────────\n\n';
  content += '结果：' + r.verdict + '\n';
  content += '理由：' + r.reason + '\n\n';
  content += '💬 ' + r.summary.replace('💬 ', '') + '\n\n';
  content += '──────────────────────────────\n';
  content += '  生成时间：' + dateStr + '\n';
  content += '  来自：等一下 · 冲动拦截器\n';
  content += '──────────────────────────────\n';

  var filename = '冲动拦截报告_' + Store.productName + '_' + price + '元.txt';

  var blob = new Blob([content], { type: 'text/plain;charset=utf-8' });
  var url = URL.createObjectURL(blob);
  var a = document.createElement('a');
  a.href = url;
  a.download = filename;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  URL.revokeObjectURL(url);

  showToast('报告已保存到本地');
}

// ═══════════════════════════════════════════
// 页面2回车键快捷提交
// ═══════════════════════════════════════════

document.getElementById('productPrice').addEventListener('keydown', function(e) {
  if (e.key === 'Enter') {
    startAnalyze();
  }
});
</script>

</body>
</html>
