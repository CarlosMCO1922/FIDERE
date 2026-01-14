# Fidere Condomínios - Website

Site institucional da Fidere Condomínios, Lda. desenvolvido em HTML, CSS e JavaScript puro.

## 📋 Características

- Design moderno e responsivo
- Transições suaves e animações
- Paleta de cores baseada no logo (laranja #FF6B35, preto #1A1A1A)
- Totalmente compatível com GitHub Pages
- Sem dependências externas (exceto Google Fonts)

## 🚀 Como Publicar no GitHub Pages

1. **Criar um repositório no GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Fidere website"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/fidere-website.git
   git push -u origin main
   ```

2. **Ativar GitHub Pages**
   - Vá às configurações do repositório (Settings)
   - Role até "Pages" no menu lateral
   - Em "Source", selecione a branch `main` e a pasta `/ (root)`
   - Clique em "Save"
   - O site estará disponível em: `https://SEU_USUARIO.github.io/fidere-website/`

## 📁 Estrutura de Ficheiros

```
Fidere/
├── index.html      # Página principal
├── styles.css      # Estilos
├── script.js       # JavaScript
├── logo.png        # Logo da empresa (a adicionar)
└── README.md       # Este ficheiro
```

## 🎨 Personalização

### Adicionar o Logo

1. Coloque o ficheiro `logo.png` na pasta raiz
2. O logo será automaticamente exibido no header

### Alterar Cores

As cores podem ser alteradas nas variáveis CSS no início do ficheiro `styles.css`:

```css
:root {
    --primary-color: #FF6B35;    /* Cor principal (laranja) */
    --primary-dark: #E55A2B;     /* Tom mais escuro */
    --secondary-color: #1A1A1A;  /* Cor secundária (preto) */
}
```

### Alterar Informações de Contacto

Edite as informações na secção de contacto no ficheiro `index.html`:

- Localização
- Email
- Telefone
- Horários de atendimento

## 📱 Responsividade

O site é totalmente responsivo e adapta-se a:
- Desktop (1200px+)
- Tablet (768px - 968px)
- Mobile (< 768px)

## 🔧 Funcionalidades

- Menu de navegação responsivo
- Scroll suave entre secções
- Formulário de contacto (frontend)
- Animações ao scroll
- Header com efeito ao scroll
- Destaque automático da secção ativa

## 📝 Notas

- O formulário de contacto atualmente apenas valida os dados no frontend. Para funcionalidade completa, será necessário integrar com um serviço de backend ou usar um serviço como Formspree, Netlify Forms, etc.

## 📄 Licença

© 2024 Fidere Condomínios, Lda. Todos os direitos reservados.
