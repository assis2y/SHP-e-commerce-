<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SHP e-commerce — Plataforma de Dropshipping</title>
<!-- Vercel Speed Insights -->
<script>
  window.si = window.si || function () { (window.siq = window.siq || []).push(arguments); };
</script>
<script defer src="/_vercel/speed-insights/script.js"></script>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  :root {
    --text-primary: #1a1a1a;
    --text-secondary: #525252;
    --text-tertiary: #737373;
    --text-quaternary: #a3a3a3;
    --border: #e5e5e5;
    --surface: #ffffff;
    --surface-muted: #f5f5f5;
    --positive: #16a34a;
    --danger: #dc2626;
    --accent: #2563eb;
    --radius-sm: 6px;
    --radius-md: 10px;
    --radius-lg: 12px;
    --space-1: 4px;
    --space-2: 8px;
    --space-3: 12px;
    --space-4: 16px;
    --space-5: 20px;
    --space-6: 24px;
    --space-8: 32px;
    --space-10: 40px;
    --space-12: 48px;
  }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    color: var(--text-primary);
    background: var(--surface);
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
  }
  .container { max-width: 720px; margin: 0 auto; padding: 0 var(--space-4); }

  /* Hero */
  .hero { text-align: center; padding: var(--space-12) 0 var(--space-8); }
  .hero-brand { display: inline-flex; align-items: center; gap: 10px; margin-bottom: var(--space-4); }
  .hero-logo {
    width: 44px; height: 44px; border-radius: var(--radius-md);
    background: var(--text-primary); display: flex; align-items: center; justify-content: center;
  }
  .hero-logo svg { width: 24px; height: 24px; }
  .hero-title { font-size: 28px; font-weight: 600; letter-spacing: 0.5px; }
  .hero-desc {
    font-size: 17px; color: var(--text-secondary); line-height: 1.5;
    max-width: 480px; margin: 0 auto var(--space-6);
  }
  .btn-primary {
    background: var(--text-primary); color: #fff; border: none;
    padding: 12px 28px; border-radius: var(--radius-md); font-size: 16px;
    font-weight: 500; cursor: pointer; font-family: inherit; text-decoration: none; display: inline-block;
    transition: opacity 0.2s;
  }
  .btn-primary:hover { opacity: 0.85; }

  /* Stats */
  .stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-3); margin-bottom: var(--space-10); }
  .stat-card {
    text-align: center; padding: var(--space-4) var(--space-2);
    border: 1px solid var(--border); border-radius: var(--radius-md);
  }
  .stat-value { font-size: 28px; font-weight: 600; font-variant-numeric: tabular-nums; }
  .stat-label { font-size: 13px; color: var(--text-tertiary); margin-top: var(--space-1); }

  /* Sections */
  .section-title {
    font-size: 20px; font-weight: 600; margin-bottom: var(--space-5); text-align: center;
  }
  .section { margin-bottom: var(--space-10); }

  /* Steps */
  .steps-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-3); }
  .step-card {
    padding: var(--space-5) var(--space-4); border: 1px solid var(--border);
    border-radius: var(--radius-lg); text-align: center;
  }
  .step-icon {
    width: 40px; height: 40px; border-radius: var(--radius-md);
    background: #f0f0f0; display: flex; align-items: center; justify-content: center;
    margin: 0 auto var(--space-3);
  }
  .step-icon svg { width: 20px; height: 20px; }
  .step-title { font-size: 15px; font-weight: 600; margin-bottom: var(--space-1); }
  .step-desc { font-size: 13px; color: var(--text-tertiary); line-height: 1.4; }

  /* Commission */
  .commission-box {
    padding: var(--space-6); border: 1px solid var(--border); border-radius: var(--radius-lg);
    background: #fafafa;
  }
  .commission-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-4); margin-bottom: var(--space-4); }
  .commission-cell {
    padding: var(--space-4); border-radius: var(--radius-md);
    background: var(--surface); border: 1px solid var(--border);
  }
  .commission-cell-label { font-size: 13px; color: var(--text-tertiary); margin-bottom: var(--space-1); }
  .commission-cell-value { font-size: 24px; font-weight: 600; font-variant-numeric: tabular-nums; }
  .commission-cell-value.negative { color: var(--danger); }
  .commission-cell-value.positive { color: var(--positive); }
  .commission-total {
    padding: var(--space-4); border-radius: var(--radius-md);
    background: var(--surface); border: 1px solid var(--border); text-align: center;
  }
  .commission-total .commission-cell-value { font-size: 28px; }
  .commission-note {
    font-size: 13px; color: var(--text-tertiary); text-align: center; margin-top: var(--space-3);
  }

  /* Benefits */
  .benefits-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-3); }
  .benefit-card {
    display: flex; gap: var(--space-3); padding: var(--space-4);
    border: 1px solid var(--border); border-radius: var(--radius-md);
  }
  .benefit-icon {
    flex-shrink: 0; width: 36px; height: 36px; border-radius: var(--radius-sm);
    background: #f0f0f0; display: flex; align-items: center; justify-content: center;
  }
  .benefit-icon svg { width: 18px; height: 18px; }
  .benefit-title { font-size: 14px; font-weight: 600; margin-bottom: 2px; }
  .benefit-desc { font-size: 12px; color: var(--text-tertiary); line-height: 1.4; }

  /* Tags */
  .tags-wrap { display: flex; flex-wrap: wrap; gap: var(--space-2); justify-content: center; }
  .tag {
    padding: 6px 14px; border-radius: var(--radius-sm);
    background: #f0f0f0; font-size: 13px; color: var(--text-secondary);
  }

  /* Testimonials */
  .testimonials-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-3); }
  .testimonial-card {
    padding: var(--space-5); border: 1px solid var(--border); border-radius: var(--radius-lg);
  }
  .stars { display: flex; gap: 4px; margin-bottom: var(--space-3); color: var(--text-primary); }
  .stars svg { width: 14px; height: 14px; }
  .testimonial-text {
    font-size: 14px; color: var(--text-secondary); line-height: 1.5; margin-bottom: var(--space-3);
  }
  .testimonial-author { display: flex; align-items: center; gap: var(--space-2); }
  .author-avatar {
    width: 32px; height: 32px; border-radius: 50%; background: var(--text-primary);
    display: flex; align-items: center; justify-content: center;
    color: #fff; font-size: 12px; font-weight: 600;
  }
  .author-name { font-size: 13px; font-weight: 600; }
  .author-niche { font-size: 11px; color: var(--text-tertiary); }

  /* Gateway */
  .gateway-box { padding: var(--space-6); border: 1px solid var(--border); border-radius: var(--radius-lg); }
  .gateway-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: var(--space-2); text-align: center; }
  .gateway-item { padding: var(--space-3) var(--space-1); border: 1px solid var(--border); border-radius: var(--radius-sm); }
  .gateway-name { font-size: 13px; font-weight: 600; }
  .gateway-desc { font-size: 11px; color: var(--text-tertiary); margin-top: 2px; }

  /* Form */
  .form-box {
    padding: var(--space-7); border: 1px solid var(--border); border-radius: var(--radius-lg);
    background: #fafafa;
  }
  .form-group { margin-bottom: var(--space-4); }
  .form-label {
    display: block; font-size: 13px; font-weight: 600; color: var(--text-secondary);
    margin-bottom: var(--space-1);
  }
  .form-input {
    width: 100%; padding: 10px 14px; border: 1px solid var(--border); border-radius: var(--radius-md);
    font-size: 15px; color: var(--text-primary); background: var(--surface); font-family: inherit;
  }
  .form-input:focus { outline: none; border-color: var(--text-primary); }
  .form-select {
    width: 100%; padding: 10px 14px; border: 1px solid var(--border); border-radius: var(--radius-md);
    font-size: 15px; color: var(--text-primary); background: var(--surface); font-family: inherit; cursor: pointer;
  }
  .form-select:focus { outline: none; border-color: var(--text-primary); }
  .form-btn {
    width: 100%; background: var(--text-primary); color: #fff; border: none;
    padding: 14px; border-radius: var(--radius-md); font-size: 16px;
    font-weight: 600; cursor: pointer; font-family: inherit; margin-top: var(--space-1);
  }
  .form-btn:hover { opacity: 0.9; }
  .success-box { display: none; text-align: center; padding: var(--space-5); }
  .success-icon {
    width: 48px; height: 48px; border-radius: 50%; background: var(--positive);
    display: flex; align-items: center; justify-content: center; margin: 0 auto var(--space-3);
  }
  .success-icon svg { width: 24px; height: 24px; }
  .success-title { font-size: 16px; font-weight: 600; margin-bottom: var(--space-1); }
  .success-desc { font-size: 14px; color: var(--text-secondary); }

  /* Footer */
  .footer { text-align: center; padding: var(--space-5) 0; border-top: 1px solid var(--border); }
  .footer-brand { display: inline-flex; align-items: center; gap: var(--space-2); margin-bottom: var(--space-2); }
  .footer-brand svg { width: 16px; height: 16px; }
  .footer-brand span { font-size: 14px; font-weight: 600; }
  .footer-copy { font-size: 12px; color: var(--text-quaternary); }

  /* Responsive */
  @media (max-width: 600px) {
    .stats-grid, .steps-grid, .commission-grid, .benefits-grid, .testimonials-grid, .gateway-grid {
      grid-template-columns: 1fr;
    }
    .hero-title { font-size: 24px; }
    .hero-desc { font-size: 15px; }
  }
</style>
</head>
<body>

<div class="container">

  <!-- Hero -->
  <section class="hero">
    <div class="hero-brand">
      <div class="hero-logo">
        <svg viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M4.1 6C4.1 5.5 4.5 5.1 5 5.1H19C19.5 5.1 19.9 5.5 19.9 6C19.9 6.5 19.5 6.9 19 6.9H5C4.5 6.9 4.1 6.5 4.1 6ZM4.1 12C4.1 11.5 4.5 11.1 5 11.1H13C13.5 11.1 13.9 11.5 13.9 12C13.9 12.5 13.5 12.9 13 12.9H5C4.5 12.9 4.1 12.5 4.1 12ZM4.1 18C4.1 17.5 4.5 17.1 5 17.1H13C13.5 17.1 13.9 17.5 13.9 18C13.9 18.5 13.5 18.9 13 18.9H5C4.5 18.9 4.1 18.5 4.1 18Z" fill="white"/></svg>
      </div>
      <span class="hero-title">SHP e-commerce</span>
    </div>
    <p class="hero-desc">A plataforma de dropshipping que conecta anunciantes de todos os nichos. Você vende, nós entregamos — e só cobramos quando vender.</p>
    <a href="#cadastro" class="btn-primary">Começar agora</a>
  </section>

  <!-- Stats -->
  <section class="section">
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-value">15%</div>
        <div class="stat-label">comissão por venda</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">0</div>
        <div class="stat-label">taxa de adesão</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">+50</div>
        <div class="stat-label">nichos ativos</div>
      </div>
    </div>
  </section>

  <!-- Como funciona -->
  <section class="section">
    <h2 class="section-title">Como funciona</h2>
    <div class="steps-grid">
      <div class="step-card">
        <div class="step-icon">
          <svg viewBox="0 0 24 24" fill="none"><path d="M19.2 9.4C20.7 9.8 21.7 11.4 21.2 12.9L19.7 18.7C19.3 20.3 17.7 21.2 16.1 20.8L11.2 19.5L14.3 18.6C14.4 18.6 14.6 18.6 14.7 18.5L16.6 19C17.2 19.2 17.8 18.8 18 18.3L19.5 12.5C19.7 11.9 19.3 11.3 18.7 11.1L15.1 10.1L14.5 8.1L19.2 9.4Z" fill="currentColor"/><path fill-rule="evenodd" clip-rule="evenodd" d="M10.2 6.6C11.7 6.2 13.3 7.1 13.7 8.7L15.3 14.4C15.7 16 14.8 17.6 13.2 18L7.4 19.6C5.9 20 4.3 19.1 3.9 17.5L2.3 11.7C1.9 10.2 2.8 8.6 4.4 8.2L10.2 6.6ZM12 9.1C11.8 8.5 11.2 8.2 10.6 8.3L4.8 9.9C4.3 10.1 3.9 10.7 4.1 11.2L5.6 17C5.8 17.6 6.4 18 7 17.8L12.8 16.3C13.4 16.1 13.7 15.5 13.5 14.9L12 9.1Z" fill="currentColor"/></svg>
        </div>
        <div class="step-title">1. Cadastre-se</div>
        <div class="step-desc">Crie sua conta gratuita em menos de 2 minutos.</div>
      </div>
      <div class="step-card">
        <div class="step-icon">
          <svg viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M12.1 2C14.2 2 16.1 2.3 17.5 2.9C18.2 3.1 18.9 3.5 19.4 3.9C19.8 4.4 20.2 5 20.2 5.7V14L20.2 14V18.1C20.2 18.8 19.8 19.4 19.4 19.9C18.9 20.3 18.2 20.7 17.5 20.9C16.1 21.5 14.2 21.8 12.1 21.8C10 21.8 8.1 21.5 6.7 20.9C6 20.7 5.3 20.3 4.8 19.9C4.4 19.4 4 18.8 4 18.1V5.7C4 5 4.4 4.4 4.8 3.9C5.3 3.5 6 3.1 6.7 2.9C8.1 2.3 10 2 12.1 2ZM18.4 16.3C18 16.5 17.6 16.7 17.2 16.9C15.7 17.4 14.1 17.6 12.1 17.6C10.1 17.6 8.5 17.4 7.1 16.9C6.6 16.7 6.2 16.5 5.8 16.3V18.1C5.8 18.2 5.8 18.3 6.1 18.5C6.3 18.8 6.7 19 7.3 19.2C8.5 19.7 10.2 20 12.1 20C14 20 15.7 19.7 16.9 19.2C17.5 19 17.9 18.8 18.1 18.5C18.4 18.3 18.4 18.2 18.4 18.1V16.3Z" fill="currentColor"/></svg>
        </div>
        <div class="step-title">2. Anuncie produtos</div>
        <div class="step-desc">Escolha produtos de qualquer nicho e publique seus anúncios.</div>
      </div>
      <div class="step-card">
        <div class="step-icon">
          <svg viewBox="0 0 24 24" fill="none"><path d="M19.3 5.9C19.7 5.6 20.2 5.6 20.6 5.9C21 6.3 21 6.8 20.6 7.2L9.7 18.1C9.3 18.4 8.7 18.4 8.4 18.1L3.4 13.1C3.1 12.8 3.1 12.2 3.4 11.9C3.8 11.5 4.3 11.5 4.7 11.9L9 16.2L19.3 5.9Z" fill="currentColor"/></svg>
        </div>
        <div class="step-title">3. Receba</div>
        <div class="step-desc">A comissão de 15% é descontada automaticamente. Você recebe o restante.</div>
      </div>
    </div>
  </section>

  <!-- Comissão -->
  <section class="section">
    <div class="commission-box">
      <h2 class="section-title">Modelo de comissão transparente</h2>
      <div class="commission-grid">
        <div class="commission-cell">
          <div class="commission-cell-label">Você vende um produto por</div>
          <div class="commission-cell-value">R$ 100,00</div>
        </div>
        <div class="commission-cell">
          <div class="commission-cell-label">Comissão SHP (15%)</div>
          <div class="commission-cell-value negative">R$ 15,00</div>
        </div>
      </div>
      <div class="commission-total">
        <div class="commission-cell-label">Você recebe na conta</div>
        <div class="commission-cell-value positive">R$ 85,00</div>
      </div>
      <p class="commission-note">Sem taxa de adesão, sem mensalidade. Só pagamos quando você vende.</p>
    </div>
  </section>

  <!-- Benefícios -->
  <section class="section">
    <h2 class="section-title">Por que anunciar na SHP?</h2>
    <div class="benefits-grid">
      <div class="benefit-card">
        <div class="benefit-icon">
          <svg viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M17 3.8H7C5.8 3.8 4.8 4.8 4.8 6V15.8C4.8 16.6 5.2 17.3 6 17.7L11 20.4C11.6 20.7 12.4 20.7 13 20.4L18 17.7C18.8 17.3 19.2 16.6 19.2 15.8V6C19.2 4.8 18.2 3.8 17 3.8ZM7 2C4.8 2 3 3.8 3 6V15.8C3 17.2 3.8 18.6 5.1 19.3L10.1 22C11.3 22.6 12.7 22.6 13.9 22L18.9 19.3C20.2 18.6 21 17.2 21 15.8V6C21 3.8 19.2 2 17 2H7Z" fill="currentColor"/><path fill-rule="evenodd" clip-rule="evenodd" d="M16.7 8.6C17.1 9 17.1 9.6 16.7 9.9L11.8 14.9C11.4 15.2 10.8 15.2 10.5 14.9L7.8 12.2C7.5 11.8 7.5 11.3 7.8 10.9C8.2 10.6 8.7 10.6 9.1 10.9L11.1 13L15.5 8.6C15.8 8.3 16.4 8.3 16.7 8.6Z" fill="currentColor"/></svg>
        </div>
        <div>
          <div class="benefit-title">Pagamento seguro</div>
          <div class="benefit-desc">Split automático via gateway integrado. Sem risco de inadimplência.</div>
        </div>
      </div>
      <div class="benefit-card">
        <div class="benefit-icon">
          <svg viewBox="0 0 24 24" fill="none"><path d="M4 3.1C4.6 3.1 5 3.5 5 4.1V18H20L20.1 18C20.6 18.1 21 18.5 21 19C21 19.6 20.6 20 20.1 20L20 20H5C3.9 20 3 19.1 3 18V4.1C3 3.5 3.4 3.1 4 3.1ZM18.3 6.5C18.6 6.1 19.3 6.1 19.7 6.4C20.1 6.8 20.1 7.4 19.8 7.9L15.9 12.2C15.2 13 13.9 13.1 13.1 12.4L10.9 10.6L7.5 14.7C7.1 15.1 6.5 15.1 6 14.8C5.6 14.4 5.6 13.8 5.9 13.4L9.4 9.3C10.1 8.5 11.3 8.4 12.2 9L14.4 10.8L18.3 6.5Z" fill="currentColor"/></svg>
        </div>
        <div>
          <div class="benefit-title">Dashboard em tempo real</div>
          <div class="benefit-desc">Acompanhe vendas, comissões e saques com gráficos atualizados ao vivo.</div>
        </div>
      </div>
      <div class="benefit-card">
        <div class="benefit-icon">
          <svg viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M4 8.1C5 7.3 6.2 7.1 7 7.1H9C9.5 7.1 9.9 7.5 9.9 8C9.9 8.5 9.5 8.9 9 8.9H7C6.5 8.9 5.7 9.1 5 9.5C4.4 10 3.9 10.7 3.9 12C3.9 13.3 4.4 14 5 14.5C5.7 14.9 6.5 15.1 7 15.1H9C9.5 15.1 9.9 15.5 9.9 16C9.9 16.5 9.5 16.9 9 16.9H7C6.2 16.9 5 16.7 4 15.9C2.9 15.2 2.1 13.9 2.1 12C2.1 10.1 2.9 8.8 4 8.1ZM14.1 8C14.1 7.5 14.5 7.1 15 7.1H17C17.8 7.1 19 7.3 20 8.1C21.1 8.8 21.9 10.1 21.9 12C21.9 13.9 21.1 15.2 20 15.9C19 16.7 17.8 16.9 17 16.9H15C14.5 16.9 14.1 16.5 14.1 16C14.1 15.5 14.5 15.1 15 15.1H17C17.5 15.1 18.3 14.9 19 14.5C19.6 14 20.1 13.3 20.1 12C20.1 10.7 19.6 10 19 9.5C18.3 9.1 17.5 8.9 17 8.9H15C14.5 8.9 14.1 8.5 14.1 8ZM7.1 12C7.1 11.5 7.5 11.1 8 11.1H16C16.5 11.1 16.9 11.5 16.9 12C16.9 12.5 16.5 12.9 16 12.9H8C7.5 12.9 7.1 12.5 7.1 12Z" fill="currentColor"/></svg>
        </div>
        <div>
          <div class="benefit-title">Integração de gateway</div>
          <div class="benefit-desc">Conecte seu gateway de pagamento favorito. Split automático de comissões.</div>
        </div>
      </div>
      <div class="benefit-card">
        <div class="benefit-icon">
          <svg viewBox="0 0 24 24" fill="none"><path d="M19.2 9.4C20.7 9.8 21.7 11.4 21.2 12.9L19.7 18.7C19.3 20.3 17.7 21.2 16.1 20.8L11.2 19.5L14.3 18.6C14.4 18.6 14.6 18.6 14.7 18.5L16.6 19C17.2 19.2 17.8 18.8 18 18.3L19.5 12.5C19.7 11.9 19.3 11.3 18.7 11.1L15.1 10.1L14.5 8.1L19.2 9.4Z" fill="currentColor"/><path fill-rule="evenodd" clip-rule="evenodd" d="M10.2 6.6C11.7 6.2 13.3 7.1 13.7 8.7L15.3 14.4C15.7 16 14.8 17.6 13.2 18L7.4 19.6C5.9 20 4.3 19.1 3.9 17.5L2.3 11.7C1.9 10.2 2.8 8.6 4.4 8.2L10.2 6.6ZM12 9.1C11.8 8.5 11.2 8.2 10.6 8.3L4.8 9.9C4.3 10.1 3.9 10.7 4.1 11.2L5.6 17C5.8 17.6 6.4 18 7 17.8L12.8 16.3C13.4 16.1 13.7 15.5 13.5 14.9L12 9.1Z" fill="currentColor"/></svg>
        </div>
        <div>
          <div class="benefit-title">Vários nichos</div>
          <div class="benefit-desc">Moda, eletrônicos, beleza, pet, casa e muito mais. Escolha seu nicho.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Nichos -->
  <section class="section">
    <h2 class="section-title">Nichos disponíveis</h2>
    <div class="tags-wrap">
      <span class="tag">Moda</span>
      <span class="tag">Eletrônicos</span>
      <span class="tag">Beleza</span>
      <span class="tag">Pet</span>
      <span class="tag">Fitness</span>
      <span class="tag">Casa & Decor</span>
      <span class="tag">Brinquedos</span>
      <span class="tag">Automotivo</span>
      <span class="tag">Papelaria</span>
      <span class="tag">+40 outros</span>
    </div>
  </section>

  <!-- Depoimentos -->
  <section class="section">
    <h2 class="section-title">O que dizem os anunciantes</h2>
    <div class="testimonials-grid">
      <div class="testimonial-card">
        <div class="stars">
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
        </div>
        <p class="testimonial-text">"Comecei a vender na SHP há 3 meses e já fiz mais de 200 vendas. O split automático é um diferencial enorme."</p>
        <div class="testimonial-author">
          <div class="author-avatar">MF</div>
          <div>
            <div class="author-name">Mariana F.</div>
            <div class="author-niche">Nicho: Beleza</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="stars">
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
        </div>
        <p class="testimonial-text">"A integração com meu gateway foi super simples. Em 1 dia já estava vendendo e recebendo automaticamente."</p>
        <div class="testimonial-author">
          <div class="author-avatar">RL</div>
          <div>
            <div class="author-name">Rafael L.</div>
            <div class="author-niche">Nicho: Eletrônicos</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="stars">
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
        </div>
        <p class="testimonial-text">"O dashboard me ajuda a entender exatamente quanto estou faturando. A transparência da comissão é nota 10."</p>
        <div class="testimonial-author">
          <div class="author-avatar">JC</div>
          <div>
            <div class="author-name">Juliana C.</div>
            <div class="author-niche">Nicho: Moda</div>
          </div>
        </div>
      </div>
      <div class="testimonial-card">
        <div class="stars">
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
          <svg viewBox="0 0 24 24" fill="none"><path d="M12 2L14.1 8.3L21 9.3L16 14.1L17.2 21L12 17.8L6.8 21L8 14.1L3 9.3L9.9 8.3L12 2Z" fill="currentColor"/></svg>
        </div>
        <p class="testimonial-text">"Não preciso me preocupar com estoque nem logística. Só foco em vender e a SHP cuida do resto."</p>
        <div class="testimonial-author">
          <div class="author-avatar">PS</div>
          <div>
            <div class="author-name">Pedro S.</div>
            <div class="author-niche">Nicho: Pet</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Gateway -->
  <section class="section">
    <div class="gateway-box">
      <h2 class="section-title">Gateway de pagamento integrado</h2>
      <p style="font-size:14px;color:var(--text-secondary);text-align:center;margin-bottom:20px;line-height:1.5;">
        A SHP se integra ao seu gateway para receber a comissão de 15% automaticamente a cada venda. Sem burocracia, sem atrasos.
      </p>
      <div class="gateway-grid">
        <div class="gateway-item">
          <div class="gateway-name">PIX</div>
          <div class="gateway-desc">Instantâneo</div>
        </div>
        <div class="gateway-item">
          <div class="gateway-name">Cartão</div>
          <div class="gateway-desc">Crédito/Débito</div>
        </div>
        <div class="gateway-item">
          <div class="gateway-name">Boleto</div>
          <div class="gateway-desc">D+1 a D+3</div>
        </div>
        <div class="gateway-item">
          <div class="gateway-name">Split</div>
          <div class="gateway-desc">Automático</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Formulário -->
  <section class="section" id="cadastro">
    <div class="form-box">
      <h2 class="section-title">Pré-cadastro de anunciante</h2>
      <p style="font-size:14px;color:var(--text-secondary);text-align:center;margin-bottom:24px;">Preencha os dados abaixo e entraremos em contato para ativar sua conta.</p>
      <form id="preCadastroForm" onsubmit="handleSubmit(event)">
        <div class="form-group">
          <label class="form-label">Nome completo</label>
          <input type="text" id="nome" required placeholder="Seu nome" class="form-input">
        </div>
        <div class="form-group">
          <label class="form-label">E-mail</label>
          <input type="email" id="email" required placeholder="seu@email.com" class="form-input">
        </div>
        <div class="form-group">
          <label class="form-label">WhatsApp</label>
          <input type="tel" id="whatsapp" required placeholder="(11) 99999-9999" class="form-input">
        </div>
        <div class="form-group">
          <label class="form-label">Nicho de interesse</label>
          <select id="niche" required class="form-select">
            <option value="">Selecione um nicho</option>
            <option value="moda">Moda</option>
            <option value="eletronicos">Eletrônicos</option>
            <option value="beleza">Beleza</option>
            <option value="pet">Pet</option>
            <option value="fitness">Fitness</option>
            <option value="casa">Casa & Decor</option>
            <option value="brinquedos">Brinquedos</option>
            <option value="automotivo">Automotivo</option>
            <option value="outro">Outro</option>
          </select>
        </div>
        <button type="submit" class="form-btn">Enviar pré-cadastro</button>
      </form>
      <div id="successMsg" class="success-box">
        <div class="success-icon">
          <svg viewBox="0 0 24 24" fill="none"><path d="M19.3 5.9C19.7 5.6 20.2 5.6 20.6 5.9C21 6.3 21 6.8 20.6 7.2L9.7 18.1C9.3 18.4 8.7 18.4 8.4 18.1L3.4 13.1C3.1 12.8 3.1 12.2 3.4 11.9C3.8 11.5 4.3 11.5 4.7 11.9L9 16.2L19.3 5.9Z" fill="white"/></svg>
        </div>
        <div class="success-title">Pré-cadastro enviado!</div>
        <div class="success-desc">Entraremos em contato em breve.</div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="footer-brand">
      <svg viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M4.1 6C4.1 5.5 4.5 5.1 5 5.1H19C19.5 5.1 19.9 5.5 19.9 6C19.9 6.5 19.5 6.9 19 6.9H5C4.5 6.9 4.1 6.5 4.1 6ZM4.1 12C4.1 11.5 4.5 11.1 5 11.1H13C13.5 11.1 13.9 11.5 13.9 12C13.9 12.5 13.5 12.9 13 12.9H5C4.5 12.9 4.1 12.5 4.1 12ZM4.1 18C4.1 17.5 4.5 17.1 5 17.1H13C13.5 17.1 13.9 17.5 13.9 18C13.9 18.5 13.5 18.9 13 18.9H5C4.5 18.9 4.1 18.5 4.1 18Z" fill="currentColor"/></svg>
      <span>SHP e-commerce</span>
    </div>
    <p class="footer-copy">Plataforma de dropshipping para anunciantes — 2026</p>
  </footer>

</div>

<script>
function handleSubmit(e) {
  e.preventDefault();
  document.getElementById('preCadastroForm').style.display = 'none';
  document.getElementById('successMsg').style.display = 'block';
}
</script>

</body>
</html>
