<template>
  <!-- Age Verification Popup -->
  <div v-if="showAgeVerification" class="age-verification-overlay">
    <div class="age-verification-modal">
      <div class="age-verification-content">
        <img src="/logopangare.png" alt="Pangare Bet" class="age-verification-logo" />
        <h2 class="age-verification-title">Pangare<span class="gold">Bet</span></h2>
        <div class="age-verification-icon">
          <span>18+</span>
        </div>
        <p class="age-verification-question">
          Você tem 18 anos ou mais?
        </p>
        <p class="age-verification-disclaimer">
          Este site contém conteúdo relacionado a apostas esportivas, 
          destinado exclusivamente para maiores de idade.
        </p>
        <div class="age-verification-buttons">
          <button @click="confirmAge" class="age-btn age-btn-yes">
            <i class="pi pi-check"></i>
            Sim, tenho 18+
          </button>
          <button @click="denyAge" class="age-btn age-btn-no">
            <i class="pi pi-times"></i>
            Não
          </button>
        </div>
        <p class="age-verification-legal">
          <i class="pi pi-shield"></i>
          Ao continuar, você confirma que tem idade legal para acessar este conteúdo.
        </p>
      </div>
    </div>
  </div>

  <div class="landing-page">
    <!-- Navigation -->
    <nav class="navbar">
      <div class="nav-container">
        <div class="logo">
          <img src="/logopangare.png" alt="Pangare Bet" class="logo-icon rounded" />
          <span class="logo-text">Pangare<span class="gold">Bet</span></span>
        </div>
        <div class="nav-links" :class="{ active: menuOpen }">
          <a href="#inicio" @click="menuOpen = false">Início</a>
          <a href="#servicos" @click="menuOpen = false">Serviços</a>
          <a href="#sobre" @click="menuOpen = false">Sobre</a>
          <a href="#depoimentos" @click="menuOpen = false">Resultados</a>
          <a href="#contato" class="btn-cta" @click="menuOpen = false">Entrar no VIP</a>
        </div>
        <button class="menu-toggle" @click="menuOpen = !menuOpen">
          <i :class="menuOpen ? 'pi pi-times' : 'pi pi-bars'"></i>
        </button>
      </div>
    </nav>

    <!-- Hero Section -->
    <section id="inicio" class="hero">
      <div class="hero-overlay"></div>
      <div class="hero-particles">
        <div v-for="n in 20" :key="n" class="particle" :style="getParticleStyle(n)"></div>
      </div>
      <div class="hero-content">
        <div class="hero-badge">
          <i class="pi pi-star-fill"></i>
          <span>Elite Horse Racing Signals</span>
        </div>
        <h1 class="hero-title">
          <span class="line1">Transforme sua</span>
          <span class="line2">Paixão por <span class="gold-text">Turfe</span></span>
          <span class="line3">em <span class="highlight">Lucro Real</span></span>
        </h1>
        <p class="hero-subtitle">
          Estratégia LAY exclusiva com 98% de acerto. Sinais VIP, mentoria especializada 
          e assessoria premium para quem busca lucro consistente em corridas de cavalos.
        </p>
        <div class="hero-stats">
          <div class="stat">
            <span class="stat-number">+98%</span>
            <span class="stat-label">Taxa de Acerto</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-number">2.500+</span>
            <span class="stat-label">Membros VIP</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-number">R$2M+</span>
            <span class="stat-label">Lucro Gerado</span>
          </div>
        </div>
        <div class="hero-cta">
          <a href="#contato" class="btn-primary">
            <i class="pi pi-crown"></i>
            Acessar Grupo VIP
          </a>
          <a href="#servicos" class="btn-secondary">
            <i class="pi pi-play-circle"></i>
            Ver Serviços
          </a>
        </div>
      </div>
      <div class="hero-visual">
        <div class="horse-silhouette"></div>
      </div>
      <div class="scroll-indicator">
        <div class="mouse">
          <div class="wheel"></div>
        </div>
        <span>Role para baixo</span>
      </div>
    </section>

    <!-- Services Section -->
    <section id="servicos" class="services">
      <div class="container">
        <div class="section-header">
          <span class="section-tag">Nossos Serviços</span>
          <h2 class="section-title">Tudo que você precisa para <span class="gold-text">vencer</span></h2>
          <p class="section-subtitle">
            Oferecemos um ecossistema completo para você lucrar com corridas de cavalos
          </p>
        </div>
        <div class="services-grid">
          <div class="service-card featured">
            <div class="service-icon">
              <i class="pi pi-crown"></i>
            </div>
            <div class="service-badge">Mais Popular</div>
            <h3>Grupo VIP de Sinais</h3>
            <p>
              Sinais exclusivos com estratégia LAY - apostamos no cavalo perdedor 
              com taxa de acerto de 98%. Análises detalhadas e resultados consistentes.
            </p>
            <ul class="service-features">
              <li><i class="pi pi-check"></i> Sinais em tempo real</li>
              <li><i class="pi pi-check"></i> Análise de odds</li>
              <li><i class="pi pi-check"></i> Gestão de banca</li>
              <li><i class="pi pi-check"></i> Suporte 24 horas</li>
            </ul>
            <a href="#contato" class="service-btn">
              Quero Participar
              <i class="pi pi-arrow-right"></i>
            </a>
          </div>
          <div class="service-card">
            <div class="service-icon mentoria">
              <i class="pi pi-users"></i>
            </div>
            <h3>Mentoria Exclusiva</h3>
            <p>
              Aprenda diretamente com profissionais que vivem do turfe há mais de 15 anos. 
              Domine as estratégias que os grandes apostadores usam.
            </p>
            <ul class="service-features">
              <li><i class="pi pi-check"></i> Aulas ao vivo semanais</li>
              <li><i class="pi pi-check"></i> Material exclusivo</li>
              <li><i class="pi pi-check"></i> Análise de performance</li>
              <li><i class="pi pi-check"></i> Comunidade privada</li>
            </ul>
            <a href="#contato" class="service-btn">
              Começar Agora
              <i class="pi pi-arrow-right"></i>
            </a>
          </div>
          <div class="service-card">
            <div class="service-icon assessoria">
              <i class="pi pi-chart-line"></i>
            </div>
            <h3>Assessoria de Investimento</h3>
            <p>
              Tenha um consultor dedicado para gerenciar sua carteira de apostas 
              com estratégias personalizadas e acompanhamento individual.
            </p>
            <ul class="service-features">
              <li><i class="pi pi-check"></i> Consultor exclusivo</li>
              <li><i class="pi pi-check"></i> Estratégia personalizada</li>
              <li><i class="pi pi-check"></i> Relatórios mensais</li>
              <li><i class="pi pi-check"></i> ROI garantido</li>
            </ul>
            <a href="#contato" class="service-btn">
              Falar com Consultor
              <i class="pi pi-arrow-right"></i>
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="sobre" class="about">
      <div class="container">
        <div class="about-grid">
          <div class="about-content">
            <span class="section-tag">Sobre Nós</span>
            <h2 class="section-title">Por que escolher a <span class="gold-text">Pangare Bet</span>?</h2>
            <p class="about-text">
              Somos uma equipe de especialistas apaixonados por turfe, com mais de 15 anos de experiência 
              em análise de corridas de cavalos. Nossa missão é democratizar o acesso a informações 
              privilegiadas e estratégias profissionais.
            </p>
            <div class="about-features">
              <div class="about-feature">
                <div class="feature-icon">
                  <i class="pi pi-shield"></i>
                </div>
                <div class="feature-content">
                  <h4>Transparência Total</h4>
                  <p>Publicamos todos os nossos resultados, ganhos e perdas.</p>
                </div>
              </div>
              <div class="about-feature">
                <div class="feature-icon">
                  <i class="pi pi-bolt"></i>
                </div>
                <div class="feature-content">
                  <h4>Análise Profissional</h4>
                  <p>Utilizamos dados, estatísticas e inteligência de mercado.</p>
                </div>
              </div>
              <div class="about-feature">
                <div class="feature-icon">
                  <i class="pi pi-heart"></i>
                </div>
                <div class="feature-content">
                  <h4>Suporte Humanizado</h4>
                  <p>Estamos sempre disponíveis para ajudar nossos membros.</p>
                </div>
              </div>
            </div>
          </div>
          <div class="about-visual">
            <div class="stats-card">
              <div class="stats-header">
                <i class="pi pi-chart-bar"></i>
                <span>Resultados do Mês</span>
              </div>
              <div class="stats-graph">
                <div class="bar" v-for="(value, index) in monthlyStats" :key="index" 
                     :style="{ height: value + '%' }" :class="{ highlight: value > 70 }">
                  <span class="bar-value">{{ value }}%</span>
                </div>
              </div>
              <div class="stats-labels">
                <span>Jan</span>
                <span>Fev</span>
                <span>Mar</span>
                <span>Abr</span>
                <span>Mai</span>
                <span>Jun</span>
              </div>
              <div class="stats-footer">
<div class="stat-item">
                <span class="label">Média Geral</span>
                <span class="value success">98.2%</span>
              </div>
                <div class="stat-item">
                  <span class="label">ROI Médio</span>
                  <span class="value success">+23.5%</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section id="depoimentos" class="testimonials">
      <div class="container">
        <div class="section-header">
          <span class="section-tag">Depoimentos</span>
          <h2 class="section-title">O que nossos <span class="gold-text">membros</span> dizem</h2>
        </div>
        <div class="testimonials-grid">
          <div class="testimonial-card" v-for="(testimonial, index) in testimonials" :key="index">
            <div class="testimonial-header">
              <div class="avatar" :style="{ background: testimonial.color }">
                {{ testimonial.initials }}
              </div>
              <div class="info">
                <h4>{{ testimonial.name }}</h4>
                <span>{{ testimonial.role }}</span>
              </div>
              <div class="rating">
                <i class="pi pi-star-fill" v-for="n in 5" :key="n"></i>
              </div>
            </div>
            <p class="testimonial-text">"{{ testimonial.text }}"</p>
            <div class="testimonial-result">
              <span class="label">Lucro no primeiro mês:</span>
              <span class="value">{{ testimonial.profit }}</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section id="contato" class="cta-section">
      <div class="cta-bg">
        <div class="cta-pattern"></div>
      </div>
      <div class="container">
        <div class="cta-wrapper">
          <div class="cta-avatar">
            <img src="/pangare.png" alt="Pangare Bet Mascote" />
          </div>
          <div class="cta-content">
            <div class="cta-icon">
              <i class="pi pi-crown"></i>
            </div>
            <h2>Pronto para começar a <span class="gold-text">lucrar</span>?</h2>
          <p>
            Entre agora para o grupo VIP e receba seu primeiro sinal em até 24 horas. 
            Garantia de 7 dias ou seu dinheiro de volta.
          </p>
          <div class="cta-buttons">
            <a href="https://wa.me/5511999999999" target="_blank" class="btn-whatsapp">
              <i class="pi pi-whatsapp"></i>
              Falar no WhatsApp
            </a>
            <a href="https://t.me/pangarebet" target="_blank" class="btn-telegram">
              <i class="pi pi-telegram"></i>
              Entrar no Telegram
            </a>
          </div>
          <div class="cta-guarantee">
            <i class="pi pi-verified"></i>
            <span>Garantia incondicional de 7 dias</span>
          </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-brand">
<div class="logo">
          <img src="/logopangare.png" alt="Pangare Bet" class="logo-avatar" />
          <span class="logo-text">Pangare<span class="gold">Bet</span></span>
        </div>
            <p>
              Transformando a paixão por turfe em resultados consistentes desde 2019.
            </p>
            <div class="social-links">
              <a href="#" aria-label="Instagram"><i class="pi pi-instagram"></i></a>
              <a href="#" aria-label="Twitter"><i class="pi pi-twitter"></i></a>
              <a href="#" aria-label="YouTube"><i class="pi pi-youtube"></i></a>
              <a href="#" aria-label="Telegram"><i class="pi pi-telegram"></i></a>
            </div>
          </div>
          <div class="footer-links">
            <div class="footer-column">
              <h4>Links Rápidos</h4>
              <a href="#inicio">Início</a>
              <a href="#servicos">Serviços</a>
              <a href="#sobre">Sobre</a>
              <a href="#contato">Contato</a>
            </div>
            <div class="footer-column">
              <h4>Serviços</h4>
              <a href="#servicos">Grupo VIP</a>
              <a href="#servicos">Mentoria</a>
              <a href="#servicos">Assessoria</a>
            </div>
            <div class="footer-column">
              <h4>Legal</h4>
              <a href="#">Termos de Uso</a>
              <a href="#">Privacidade</a>
              <a href="#">Cookies</a>
            </div>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; 2025 Pangare Bet. Todos os direitos reservados.</p>
          <p class="disclaimer">
            Aposte com responsabilidade. Este serviço é destinado a maiores de 18 anos.
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const menuOpen = ref(false)
const showAgeVerification = ref(false)

// Check age verification on mount
onMounted(() => {
  const isAgeVerified = localStorage.getItem('pangarebet_age_verified')
  if (!isAgeVerified) {
    showAgeVerification.value = true
    document.body.style.overflow = 'hidden'
  }
})

const confirmAge = () => {
  localStorage.setItem('pangarebet_age_verified', 'true')
  showAgeVerification.value = false
  document.body.style.overflow = ''
}

const denyAge = () => {
  window.location.href = 'https://www.google.com'
}

const monthlyStats = [97, 98, 99, 96, 98, 100]

const testimonials = [
  {
    name: 'Carlos Mendes',
    role: 'Membro VIP há 8 meses',
    initials: 'CM',
    color: 'linear-gradient(135deg, #D4AF37 0%, #FFD700 100%)',
    text: 'Nunca imaginei que seria possível ter resultados tão consistentes. A equipe é extremamente profissional e os sinais são precisos.',
    profit: '+R$ 12.450'
  },
  {
    name: 'Ana Paula Silva',
    role: 'Membro VIP há 1 ano',
    initials: 'AS',
    color: 'linear-gradient(135deg, #8B5CF6 0%, #A78BFA 100%)',
    text: 'A mentoria mudou completamente minha visão sobre apostas em turfe. Hoje tenho uma renda extra significativa todo mês.',
    profit: '+R$ 8.900'
  },
  {
    name: 'Roberto Almeida',
    role: 'Assessoria Premium',
    initials: 'RA',
    color: 'linear-gradient(135deg, #10B981 0%, #34D399 100%)',
    text: 'O suporte personalizado da assessoria é impecável. Meu consultor está sempre disponível e os resultados falam por si.',
    profit: '+R$ 28.300'
  }
]

const getParticleStyle = (n) => {
  const delay = Math.random() * 5
  const duration = 3 + Math.random() * 4
  const left = Math.random() * 100
  const size = 2 + Math.random() * 4
  return {
    left: `${left}%`,
    width: `${size}px`,
    height: `${size}px`,
    animationDelay: `${delay}s`,
    animationDuration: `${duration}s`
  }
}
</script>

<style scoped>
/* All styles are in style.css */
</style>

