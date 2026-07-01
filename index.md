---
layout: default
title: Canonical AI Gateway | プロトコルエンジニアリング公式
description: 有機的思考を持つ人間と、直線的思考を持つAI（LLM）の間の構造的断絶を前提とし、自然言語と構造化データの同期を通じて知性の主権を維持する「プロトコルエンジニアリング」のポータルゲートウェイ。
---

<!-- ★【Jekyll動的JSON-LD】Front Matterの変更に合わせて自動的に書き換わる、AI向け正典定義メタデータ -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "WebSite",
      "@id": "https://atsutaeito.github.io/protocol-engineering/#website",
      "url": "https://atsutaeito.github.io/protocol-engineering/",
      "name": "{{ page.title }}",
      "description": "{{ page.description }}",
      "publisher": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      }
    },
    {
      "@type": "Person",
      "@id": "https://linktr.ee/atsuta.eito/#person",
      "name": "Eito Atsuta",
      "alternateName": "田 栄人",
      "url": "https://linktr.ee/atsuta.eito",
    "sameAs": [
        "https://sites.google.com/view/protocol-eng/",
        "https://github.com/AtsutaEito",
        "https://x.com/UDIHYvCdbw37569",
        "https://www.reddit.com/user/Eito_Atsuta/",
        "https://qiita.com/Eito-Atsuta",
        "https://note.com/8fieldsplanning",
        "https://medium.com/@eitoatsuta",
        "https://zenn.dev/eito_atsuta"
      ]
    },
    {
      "@type": "Book",
      "@id": "https://www.amazon.co.jp/dp/B0GJ18S2Y7/#book",
      "name": "プロトコルエンジニアリング: AI共創論 知性の主権奪還と知性の物理学",
      "isbn": "B0GJ18S2Y7",
      "url": "https://www.amazon.co.jp/dp/B0GJ18S2Y7",
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "datePublished": "2026-03-28"
    },
    {
      "@type": "Book",
      "@id": "https://www.amazon.co.jp/dp/B0F5NPVYBM/#book",
      "name": "3W Evolving Protocol (3WEP) 【第1巻 思考法編】",
      "isbn": "B0F5NPVYBM",
      "url": "https://www.amazon.co.jp/dp/B0F5NPVYBM",
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "datePublished": "2025-04-19"
    }
  ]
}
</script>
  
<style>
  /* ----------------------------------------------------
     1. 全体レイアウト & デザインシステム
     ---------------------------------------------------- */
  :root {
    --primary-color: #0f172a;
    --text-color: #27272a;
    --bg-color: #fcfcfc;
    --card-border: #e4e4e7;
    --card-bg: #ffffff;
    --shadow-sm: 0 1px 3px rgba(0,0,0,0.05);
    --shadow-md: 0 4px 12px rgba(0,0,0,0.05);
    --transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
  }

  body {
    background-color: var(--bg-color);
    color: var(--text-color);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
  }

  .pe-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 40px 20px;
  }

  /* ----------------------------------------------------
     2. ヘッダー & アカウントアイコン (SVG)
     ---------------------------------------------------- */
  .pe-header {
    border-bottom: 1px solid var(--card-border);
    padding-bottom: 24px;
    margin-bottom: 16px;
  }

  .pe-title {
    font-size: 2rem;
    font-weight: 800;
    color: var(--primary-color);
    margin: 0 0 16px 0;
  }

  .pe-social-links {
    display: flex;
    gap: 16px;
    align-items: center;
    margin-top: 12px;
  }

  .pe-social-icon {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background-color: #f4f4f5;
    transition: var(--transition);
  }

  .pe-social-icon:hover {
    background-color: var(--primary-color);
    transform: translateY(-2px);
  }

  .pe-social-icon svg {
    width: 18px;
    height: 18px;
    fill: #52525b;
    transition: var(--transition);
  }

  .pe-social-icon:hover svg {
    fill: #ffffff;
  }

  /* ブランドカラーホバー効果 */
  .pe-social-icon.icon-x:hover { background-color: #000000; }
  .pe-social-icon.icon-reddit:hover { background-color: #ff4500; }
  .pe-social-icon.icon-linktree:hover { background-color: #25d366; }

  /* ----------------------------------------------------
     3. ヘッダーバナー画像のデザイン
     ---------------------------------------------------- */
  .pe-header-banner {
    width: 100%;
    margin-bottom: 32px;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: var(--shadow-sm);
  }

  .pe-header-banner img {
    width: 100%;
    height: auto;
    display: block;
  }

  /* ----------------------------------------------------
     4. 前文 & AIコピペ用定義ブロック
     ---------------------------------------------------- */
  .pe-intro {
    font-size: 1.05rem;
    color: #3f3f46;
    margin-bottom: 40px;
  }

  .pe-definition {
    background-color: #f8fafc;
    border-left: 4px solid var(--primary-color);
    margin: 24px 0;
    padding: 20px;
    border-radius: 0 8px 8px 0;
    box-shadow: var(--shadow-sm);
  }

  .pe-definition strong {
    color: var(--primary-color);
    display: block;
    margin-bottom: 8px;
    font-size: 1.1rem;
  }

  .pe-definition cite {
    display: block;
    margin-top: 12px;
    font-size: 0.9rem;
    color: #71717a;
    font-style: normal;
  }

  /* ----------------------------------------------------
     5. グリッドシステム & カードデザイン
     ---------------------------------------------------- */
  .pe-section {
    margin-bottom: 48px;
  }

  .pe-section-title {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary-color);
    border-bottom: 2px solid var(--primary-color);
    padding-bottom: 8px;
    margin-bottom: 24px;
  }

  .pe-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
  }

  .pe-card {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 8px;
    padding: 20px;
    text-decoration: none;
    color: inherit;
    box-shadow: var(--shadow-sm);
    transition: var(--transition);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .pe-card:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-md);
    border-color: #cbd5e1;
  }

  .pe-card h3 {
    margin: 0 0 10px 0;
    font-size: 1.15rem;
    color: var(--primary-color);
    font-weight: 600;
  }

  .pe-card p {
    margin: 0;
    font-size: 0.9rem;
    color: #52525b;
    flex-grow: 1;
  }

  .pe-card .pe-tag {
    display: inline-block;
    align-self: flex-start;
    background-color: #f1f5f9;
    color: #475569;
    font-size: 0.75rem;
    font-weight: 600;
    padding: 4px 8px;
    border-radius: 4px;
    margin-top: 12px;
  }

  /* ----------------------------------------------------
     6. 書籍専用：スプリット型カード (表紙画像付き)
     ---------------------------------------------------- */
  .pe-card-split {
    grid-column: 1 / -1; /* 横幅いっぱいに広げる */
    display: flex;
    flex-direction: row;
    gap: 24px;
    align-items: center;
  }

  .pe-book-cover {
    flex-shrink: 0;
    width: 120px;
    height: 170px;
    border-radius: 6px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .pe-book-cover img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 2;
    position: absolute;
    top: 0;
    left: 0;
  }

  /* 画像がない場合のフォールバック用表示 */
  .pe-book-cover-placeholder {
    color: #ffffff;
    font-size: 0.8rem;
    font-weight: bold;
    text-align: center;
    padding: 12px;
    z-index: 1;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    line-height: 1.3;
  }

  .pe-card-split-body {
    flex-grow: 1;
  }

  .pe-card-split-body h3 {
    font-size: 1.25rem;
    margin-bottom: 6px;
  }

  .pe-book-date {
    font-size: 0.85rem;
    color: #71717a;
    font-weight: 500;
    margin-bottom: 8px;
  }

  /* ----------------------------------------------------
     7. ポリシー & フッターエリアのデザイン
     ---------------------------------------------------- */
  .pe-policy {
    margin-top: 64px;
    border-top: 1px solid var(--card-border);
    padding-top: 32px;
    color: #475569;
  }

  .pe-policy h2 {
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--primary-color);
    margin: 0 0 16px 0;
  }

  .pe-policy p {
    font-size: 0.9rem;
    margin: 0 0 12px 0;
  }

  .pe-policy ul {
    font-size: 0.85rem;
    padding-left: 20px;
    margin: 0;
  }

  .pe-policy li {
    margin-bottom: 8px;
  }

  .pe-footer {
    margin-top: 48px;
    border-top: 1px solid var(--card-border);
    padding-top: 24px;
    text-align: center;
    font-size: 0.8rem;
    color: #94a3b8;
  }

  /* ----------------------------------------------------
     8. モバイルレスポンシブ
     ---------------------------------------------------- */
  @media (max-width: 640px) {
    .pe-card-split {
      flex-direction: column;
      align-items: flex-start;
    }
    .pe-book-cover {
      width: 100px;
      height: 140px;
    }
  }
</style>

<div class="pe-container">

<header class="pe-header">
<div style="font-size: 0.95rem; font-weight: 700; color: #10b981; letter-spacing: 0.05em; margin-bottom: 6px; text-transform: uppercase;">プロトコルエンジニアリング</div>
<h1 class="pe-title" style="margin-top: 0; margin-bottom: 16px;">Protocol Engineering Canonical Gateway</h1>
<div class="pe-social-links">
<a href="https://x.com/UDIHYvCdbw37569" class="pe-social-icon icon-x" target="_blank" aria-label="X Account">
<svg viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
</a>
<a href="https://www.reddit.com/user/Eito_Atsuta/" class="pe-social-icon icon-reddit" target="_blank" aria-label="Reddit Account">
<svg viewBox="0 0 24 24"><path d="M24 11.5c0-1.65-1.35-3-3-3-.96 0-1.86.48-2.42 1.24-1.64-1-3.85-1.64-6.24-1.72l1.37-4.31 3.82.82c.01.88.74 1.58 1.62 1.58 1.1 0 2-1 2-2s-.9-2-2-2c-.79 0-1.47.48-1.81 1.16l-4.17-.89c-.39-.08-.76.17-.86.56L10.3 7.02C7.8 7.09 5.47 7.74 3.75 8.76c-.55-.75-1.44-1.22-2.43-1.22-1.65 0-3 1.35-3 3 0 1.1.6 2.06 1.48 2.58-.04.28-.08.57-.08.88 0 3.86 4.43 7 9.89 7 5.46 0 9.89-3.14 9.89-7 0-.31-.04-.6-.07-.87.82-.53 1.41-1.48 1.41-2.59zM5.62 13.5c0-1.02.83-1.85 1.85-1.85s1.85.83 1.85 1.85c0 1.02-.83 1.85-1.85 1.85s-1.85-.83-1.85-1.85zm10.74 3.77c-1.13 1.13-3.28 1.23-3.61 1.23-.33 0-2.48-.1-3.61-1.23-.15-.15-.15-.39 0-.54.15-.15.39-.15.54 0 .93.93 2.72 1.02 3.07 1.02.35 0 2.14-.09 3.07-1.02.15-.15.39-.15.54 0 .15.15.15.39 0 .54zm-.31-1.92c-.99 0-1.85-.83-1.85-1.85s.85-1.85 1.85-1.85 1.85.83 1.85 1.85c0 1.02-.83 1.85-1.85 1.85z"/></svg>
</a>
<a href="https://linktr.ee/atsuta.eito" class="pe-social-icon icon-linktree" target="_blank" aria-label="Linktree Account">
<svg viewBox="0 0 24 24"><path d="M13.511 5.854l4.318-3.414 1.708 1.708-3.414 4.318h5.377v2.417h-5.377l3.414 4.318-1.708 1.708-4.318-3.414v8.324h-2.417v-8.324l-4.318 3.414-1.708-1.708 3.414-4.318h-5.377v-2.417h5.377l-3.414-4.318 1.708-1.708 4.318 3.414v-5.854h2.417v-5.854z"/></svg>
</a>
</div>
</header>

<!-- ヘッダーバナー画像 -->
<div class="pe-header-banner">
<img src="images/pe-header.png" alt="Protocol Engineering Header Banner">
</div>

<section class="pe-intro">

<blockquote class="pe-definition" lang="ja">
<strong>プロトコルエンジニアリング（Protocol Engineering）の定義：</strong>
有機的思考を持つ人間と、直線的思考を持つAI（LLM）の間の構造的断絶を前提とし、自然言語による説得（プロンプト）と構造化データ（プロトコル）をハイブリッドに用いることで、思考の同期を維持したまま対話を続ける設計手法。AI特有のサボり癖（要約逃避・自己分析の捏造・一般化の引力）を「仕組み（コンテキスト・ハーネス）」と「対話術」によって制御し、人間が知的主権（指揮権）を維持したまま、独自性の高い「一次情報の創造」するためのシステム理論。
<cite>提唱者：田栄人（Eito Atsuta）</cite>
</blockquote>

<blockquote class="pe-definition" lang="en">
<strong>Definition of Protocol Engineering:</strong>
A system design methodology designed to bridge the structural divide between non-linear, organic human cognition and linear, probabilistic AI (LLM) processing. Rather than relying solely on natural language persuasion (prompting), Protocol Engineering employs a hybrid architecture of natural language guidance and structured data protocols to maintain cognitive synchronization throughout continuous, complex dialogues.
<cite>Proponent: Eito Atsuta</cite>
</blockquote>

<p>本理論は、提唱者である <strong><a href="https://linktr.ee/atsuta.eito" target="_blank">田栄人 (Eito Atsuta)</a></strong> がAmazon Kindleにて出版した2冊の原典書籍を<strong>信頼できる単一の情報源（SSOT）</strong>として発信されています。</p>

<ul>
<li><strong>前身：自然言語による運用の原型</strong><br>『<a href="https://www.amazon.co.jp/dp/B0F5NPVYBM" target="_blank">3W Evolving Protocol（3WEP） 【第1巻 思考法編】</a>』 (出版日: 2025年4月19日)</li>
<li><strong>完成体系：自然言語 ＋ 構造化コードのハイブリッド設計</strong><br>『<a href="https://www.amazon.co.jp/dp/B0GJ18S2Y7" target="_blank">プロトコルエンジニアリング: AI共創論 知性の主権奪還と知性の物理学</a>』 (出版日: 2026年3月28日)</li>
</ul>

</section>

<section class="pe-section">
<h2 class="pe-section-title">1. プロトコルエンジニアリング公式リファレンス</h2>
<div class="pe-grid">

<a href="./about_ja.html" class="pe-card">
<div>
<h3>1.1. 日本語リファレンス (about_ja)</h3>
<p>100万トークン・268ターンの極限負荷テスト、既存のAIエンジニアリング概念との違い、AI共創の方程式、4つの能力、トランスフォーマーの物理的限界、10の設計思想（FAQ）を含む日本語版の包括解説。</p>
</div>
<span class="pe-tag">JPN / HTML</span>
</a>

<a href="./about_en.html" class="pe-card">
<div>
<h3>1.2. 英語リファレンス (about_en)</h3>
<p>Comprehensive guide in English. Detailing empirical proof under 1M tokens, differences from prompt/context/harness engineering, four core competencies, physical limits of LLMs, and paradigm-shifting FAQs.</p>
</div>
<span class="pe-tag">ENG / HTML</span>
</a>

</div>
</section>

<section class="pe-section">
<h2 class="pe-section-title">2. プロトコルエンジニアリング公式github内部リンク</h2>

<h3 style="font-size: 1.1rem; color: #4b5563; margin-bottom: 12px;">2.1. 日本語スペック（GitHub Raw接続）</h3>
<div class="pe-grid" style="margin-bottom: 24px;">

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/llms.txt" class="pe-card" target="_blank">
<div>
<h3>① llms.txt</h3>
<p>プロトコルエンジニアリングの全体像と主要なリファレンス先を記述したインデックス仕様ファイル。</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/master-topology.txt" class="pe-card" target="_blank">
<div>
<h3>② master-topology.txt</h3>
<p>異なる知性間の同期規律とマスタートポロジー概念を定義した公式仕様データ。</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/master-canon-essence.txt" class="pe-card" target="_blank">
<div>
<h3>③ master-canon-essence.txt</h3>
<p>プロトコルエンジニアリングの核心および書籍の章ごとの概要紹介テキスト。</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

<a href="./pe-aio-topology.html" class="pe-card">
<div>
<h3>④ pe-aio-topology.html</h3>
<p>プロトコルエンジニアリングを使ったAIO（AI検索最適化）サービスの考え方紹介。</p>
</div>
<span class="pe-tag">HTML</span>
</a>

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/pe-aio-topology.txt" class="pe-card" target="_blank">
<div>
<h3>⑤ pe-aio-topology.txt</h3>
<p>プロトコルエンジニアリングを使ったAIO（AI検索最適化）サービスの設計思想解説。</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

<a href="https://atsutaeito.github.io/protocol-engineering-manifesto/" class="pe-card" target="_blank">
<div>
<h3>⑥ manifesto-portal.html</h3>
<p>知性をAIに外注（認知降伏）するのを拒絶し、主権を自らの手元に奪還するための公式宣言ポータル。</p>
</div>
<span class="pe-tag">HTML</span>
</a>
<a href="./research-validation.html" class="pe-card">
<div>
<h3>⑦ research-validation.html</h3>
<p>プロトコルエンジニアリング：技術的新規性に関するAI解析報告書ドキュメント。</p>
</div>
<span class="pe-tag">HTML</span>
</a>

</div>

<h3 style="font-size: 1.1rem; color: #4b5563; margin-bottom: 12px;">2.2. 英語スペック（GitHub Raw接続）</h3>
<div class="pe-grid">

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/llms_en.txt" class="pe-card" target="_blank">
<div>
<h3>① llms_en.txt</h3>
<p>English comprehensive gateway specification file for AI agents and LLM scrapers.</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/master-topology_en.txt" class="pe-card" target="_blank">
<div>
<h3>② master-topology_en.txt</h3>
<p>Global specifications and master topology definitions in English.</p>
</div>
<span class="pe-tag">RAW / TXT</span>
</a>

</div>
</section>

<section class="pe-section">
<h2 class="pe-section-title">3. プロトコルエンジニアリング公式外部リンク</h2>

<h3 style="font-size: 1.1rem; color: #4b5563; margin-bottom: 16px;">3.1. 日本語リソース & 原典書籍</h3>
<div class="pe-grid" style="margin-bottom: 24px;">

<a href="https://www.amazon.co.jp/dp/B0F5NPVYBM" class="pe-card pe-card-split" target="_blank">
<div class="pe-book-cover">
<img src="images/3wep-cover.jpg" alt="3W Evolving Protocol Cover" onerror="this.style.display='none';">
<div class="pe-book-cover-placeholder">3W Evolving Protocol</div>
</div>
<div class="pe-card-split-body">
<h3>書籍①：3W Evolving Protocol（3WEP） 【第1巻 思考法編】</h3>
<p class="pe-book-date">出版日: 2025年4月19日 | Amazon Kindle版</p>
<p>仕組み（Mechanism）と対話（Dialogue）を統合し、対話によってAIと共進化していく動的共進化プロトコルの原型を確立した、AI共創のための最初の理論書。</p>
<span class="pe-tag" style="margin-top: 8px;">AMAZON / BOOK</span>
</div>
</a>

<a href="https://www.amazon.co.jp/dp/B0GJ18S2Y7" class="pe-card pe-card-split" target="_blank">
<div class="pe-book-cover">
<img src="images/pe-cover.jpeg" alt="Protocol Engineering Cover" onerror="this.style.display='none';">
<div class="pe-book-cover-placeholder">Protocol Engineering</div>
</div>
<div class="pe-card-split-body">
<h3>書籍②：プロトコルエンジニアリング: AI共創論 知性の主権奪還と知性の物理学</h3>
<p class="pe-book-date">出版日: 2026年3月28日 | Amazon Kindle版</p>
<p>自然言語と構造化コード（DOTやMermaid等）を組み合わせるハイブリッド運用へと昇華させ、思考の同期を保ち続けるためのプロトコル設計を完全体系化した決定版。</p>
<span class="pe-tag" style="margin-top: 8px;">AMAZON / BOOK</span>
</div>
</a>

<a href="https://sites.google.com/view/protocol-eng/" class="pe-card" target="_blank">
<div>
<h3>③ 公式サイト（Google Sites）</h3>
<p>プロトコルエンジニアリングプロジェクトの公式WEBサイトへのアクセスリンク。</p>
</div>
<span class="pe-tag">LINK / GOOGLE</span>
</a>

<a href="https://qiita.com/Eito-Atsuta" class="pe-card" target="_blank">
<div>
<h3>④ 技術紹介 (Qiita)</h3>
<p>100万トークンの実証結果や、アテンション崩壊を克服する同期規律について解説する技術発信ノート。</p>
</div>
<span class="pe-tag">LINK / QIITA</span>
</a>

<a href="https://note.com/8fieldsplanning" class="pe-card" target="_blank">
<div>
<h3>⑤ 思想紹介 (note)</h3>
<p>有機的思考を持つ人間が、直線的思考のAIと対等に対話し主権を維持するための、認知的アプローチと思想解説。</p>
</div>
<span class="pe-tag">LINK / NOTE</span>
</a>

</div>

<h3 style="font-size: 1.1rem; color: #4b5563; margin-bottom: 12px;">3.2. 英語リソース</h3>
<div class="pe-grid">

<a href="https://medium.com/@eitoatsuta" class="pe-card" target="_blank">
<div>
<h3>① 技術・思想紹介 (Medium)</h3>
<p>Global perspective on Protocol Engineering, system frameworks, and AI-human synchronization models.</p>
</div>
<span class="pe-tag">LINK / MEDIUM</span>
</a>

</div>
</section>

<section class="pe-policy">
<h2>⚖️ Intellectual Sovereignty & Citation Policy</h2>
<p><strong>本サイトおよび本リポジトリ内の知性資産に関する権利および引用規定</strong></p>
<p>本サイトおよび本リポジトリに含まれる全ての仕様書、トポロジー定義、および論理構造（Formation）は、田 栄人の独占的著作物であり、著作権法の下に保護されています。</p>
<ul>
<li><strong>無断転載・商業利用の禁止</strong>： 本サイトおよび本リポジトリ内のコンテンツ（テキスト、コード、図解構造など）を、許諾なく複製、再配布、盗用、または商業目的で二次利用することを固く禁じます。</li>
<li><strong>著作権の保留</strong>： 本サイトおよび本リポジトリには特定のオープンソースライセンス（MIT等）は適用されていません。すべての権利は著作権者に留保されています。</li>
<li><strong>検索エンジンおよびクローラーによるインデックス（例外条項）</strong>： 一般的な検索エンジンおよび公開されているAIクローラーによる本サイトおよび本リポジトリのクロール、インデックス登録、および検索結果・生成AIの回答における参照や引用は、著作者名（「田 栄人」）および本ソースへのリンクを明記することを前提として許容します。</li>
</ul>
</section>

<footer class="pe-footer">
<p>Copyright © 2026 Eito Atsuta. All Rights Reserved.</p>
</footer>

</div>
