# 🎨 CSS e JavaScript Base - InkTec

Este é o sistema de design base para todas as páginas do site InkTec, garantindo consistência visual e funcional em todo o projeto.

## 📁 Arquivos Incluídos

- **`styles.css`** - CSS base com todos os estilos padrão
- **`scripts.js`** - JavaScript base com funcionalidades comuns
- **`README-CSS-BASE.md`** - Este arquivo de instruções

## 🚀 Como Usar

### 1. Incluir os Arquivos Base

Adicione estes links no `<head>` de todas as páginas:

```html
<!-- CSS Base -->
<link rel="stylesheet" href="styles.css">

<!-- Font Awesome (para ícones) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<!-- JavaScript Base (antes do fechamento do </body>) -->
<script src="scripts.js"></script>
```

### 2. Estrutura HTML Padrão

Use esta estrutura base em todas as páginas:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título da Página - InkTec</title>
    
    <!-- CSS Base -->
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <!-- Header Padrão -->
    <header>
        <div class="container header-container">
            <div class="header-top">
                <div class="logo">
                    <img src="https://i.postimg.cc/76Ngdx1Q/LOGO-DO-CABE-ALHO.png" alt="InkTec Logo">
                    <div class="logo-text">InkTec Automação</div>
                </div>
                <button class="mobile-toggle">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="index.html">Início</a></li>
                    <li><a href="index.html#quem-somos">Quem Somos</a></li>
                    <li><a href="index.html#solucoes">Soluções</a></li>
                    <li><a href="index.html#ia">IA</a></li>
                    <li><a href="index.html#contato">Contato</a></li>
                    <li><a href="download.html">Download</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Conteúdo da Página -->
    <main>
        <!-- Suas seções aqui -->
    </main>

    <!-- Footer Padrão -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <!-- Conteúdo do footer -->
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 InkTec. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript Base -->
    <script src="scripts.js"></script>
</body>
</html>
```

## 🎯 Classes CSS Disponíveis

### Containers e Layout
- `.container` - Container principal (max-width: 1200px)
- `.section` - Seção padrão com padding
- `.grid` - Grid responsivo
- `.grid-2`, `.grid-3`, `.grid-4` - Grids com 2, 3 ou 4 colunas

### Componentes
- `.card` - Card padrão com hover effects
- `.btn` - Botão principal
- `.btn-outline` - Botão outline
- `.section-header` - Cabeçalho de seção
- `.section-title` - Título de seção
- `.section-subtitle` - Subtítulo de seção

### Utilitários
- `.text-center`, `.text-left`, `.text-right` - Alinhamento de texto
- `.mb-0` até `.mb-5` - Margens bottom
- `.mt-0` até `.mt-5` - Margens top
- `.p-0` até `.p-5` - Paddings
- `.d-none`, `.d-block`, `.d-flex`, `.d-grid` - Display
- `.justify-center`, `.justify-between` - Justify content
- `.align-center`, `.align-start`, `.align-end` - Align items
- `.w-100`, `.h-100` - Width e height 100%
- `.rounded`, `.rounded-lg`, `.rounded-xl` - Border radius
- `.shadow`, `.shadow-lg` - Box shadows

## ⚡ Funcionalidades JavaScript Incluídas

### Automáticas
- ✅ Menu mobile toggle
- ✅ Smooth scrolling para links internos
- ✅ Header scroll effect
- ✅ Animações de entrada (Intersection Observer)
- ✅ Validação de formulários
- ✅ Validação de email
- ✅ Lazy loading de imagens
- ✅ Botão "Voltar ao topo"
- ✅ Preloader (se existir)

### Opcionais (com data attributes)
- `data-target="100"` - Animação de contador
- `data-tooltip="Texto do tooltip"` - Tooltip
- `data-modal="modal-id"` - Abrir modal
- `data-src="imagem.jpg"` - Lazy loading
- `data-parallax="0.5"` - Efeito parallax
- `data-typing="Texto para digitar"` - Animação de digitação

## 🎨 Variáveis CSS Disponíveis

```css
:root {
    --primary: #0056b3;      /* Azul principal */
    --primary-dark: #004494; /* Azul escuro */
    --secondary: #00a0e3;    /* Azul claro */
    --light: #f8f9fa;        /* Cinza claro */
    --dark: #343a40;         /* Cinza escuro */
    --gray: #6c757d;         /* Cinza médio */
    --white: #ffffff;        /* Branco */
    --success: #28a745;      /* Verde */
    --danger: #dc3545;       /* Vermelho */
}
```

## 📱 Responsividade

O sistema é totalmente responsivo com breakpoints:
- **Desktop**: > 1200px
- **Tablet**: 768px - 1200px
- **Mobile**: < 768px
- **Mobile pequeno**: < 576px

## 🔧 Personalização

### Adicionar CSS Específico da Página

```html
<style>
    /* Seus estilos específicos aqui */
    .minha-classe {
        /* Estilos personalizados */
    }
</style>
```

### Usar Funções JavaScript Globais

```javascript
// Animação de contador
InkTecUtils.animateCounter(element, 1000);

// Validação de email
InkTecUtils.isValidEmail('email@exemplo.com');

// Debounce
const debouncedFunction = InkTecUtils.debounce(function() {
    // Sua função aqui
}, 300);

// Throttle
const throttledFunction = InkTecUtils.throttle(function() {
    // Sua função aqui
}, 100);
```

## 📋 Checklist para Novas Páginas

- [ ] Incluir `styles.css` no `<head>`
- [ ] Incluir `scripts.js` antes do `</body>`
- [ ] Usar estrutura HTML padrão (header + main + footer)
- [ ] Usar classes CSS base quando possível
- [ ] Testar responsividade
- [ ] Verificar se todas as funcionalidades JavaScript funcionam

## 🎯 Exemplos de Uso

### Criar uma Seção Padrão
```html
<section class="section">
    <div class="container">
        <div class="section-header">
            <h2 class="section-title">Meu Título</h2>
            <p class="section-subtitle">Meu subtítulo</p>
        </div>
        <div class="grid grid-3">
            <div class="card">
                <h3>Card 1</h3>
                <p>Conteúdo do card</p>
            </div>
            <div class="card">
                <h3>Card 2</h3>
                <p>Conteúdo do card</p>
            </div>
            <div class="card">
                <h3>Card 3</h3>
                <p>Conteúdo do card</p>
            </div>
        </div>
    </div>
</section>
```

### Criar um Botão
```html
<a href="#contato" class="btn">
    <i class="fas fa-envelope"></i>
    Entre em Contato
</a>
```

### Criar um Contador Animado
```html
<div class="card text-center">
    <h3>Clientes Atendidos</h3>
    <div class="number" data-target="1500">0</div>
</div>
```

## 🚨 Importante

- **Sempre** use as classes CSS base quando possível
- **Mantenha** a estrutura HTML padrão
- **Teste** a responsividade em diferentes dispositivos
- **Não** sobrescreva estilos base sem necessidade
- **Use** as variáveis CSS para cores e espaçamentos

---

**Desenvolvido para InkTec Automação** 🚀 