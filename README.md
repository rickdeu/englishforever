# 🌐 English Forever - Website Oficial

## 📋 Sobre o Projeto

Website profissional para a **English Forever**, uma escola de inglês moderna e prática focada em resultados reais, oferecendo cursos de inglês, serviços de tradução juramentada e interpretação profissional.

**Live Preview:** [https://english-forever-website.netlify.app/](https://english-forever-website.netlify.app/)

---

## ✨ Características Principais

### 🎨 Design & Interface
- ✅ Design moderno e profissional com cores corporativas (azul escuro, branco e vermelho)
- ✅ Totalmente responsivo para todos os dispositivos (desktop, tablet, mobile)
- ✅ Navegação intuitiva com menu fixo
- ✅ Banner/slider de imagens em tela cheia
- ✅ Animações suaves e transições

### 🌐 Sistema de Idioma Duplo
- ✅ Português e Inglês integrados
- ✅ Botão de seleção de idioma no menu
- ✅ Todo conteúdo traduzido automaticamente
- ✅ Formulários e elementos interativos bilíngues

### 📝 Formulário de Contacto Funcional
- ✅ Integração com Formspree para envio automático de emails
- ✅ Validação de campos em tempo real
- ✅ Feedback visual (loading, sucesso, erro)
- ✅ Envia automaticamente para: `englishforevernopt@gmail.com`

### 📊 Seções Completas
1. **Home** - Banner com slider de imagens
2. **Sobre Nós** - Missão, visão e valores
3. **Cursos** - 4 tipos de cursos detalhados
4. **Tradução** - Serviços de tradução juramentada e técnica
5. **Interpretação** - Serviços de interpretação simultânea, consecutiva e online
6. **Depoimentos** - Testemunhos de clientes
7. **Contacto** - Informações e formulário funcional

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilos avançados com variáveis CSS
- **JavaScript (Vanilla)** - Funcionalidades interativas
- **Swiper.js** - Slider de imagens responsivo
- **Font Awesome** - Ícones
- **Formspree** - Processamento de formulários
- **Google Fonts** - Tipografia moderna

---

## 🚀 Como Usar

### 1. Usar o Site Pronto
O site está completamente funcional. Basta:
- Copiar todo o código HTML
- Salvar como `index.html`
- Abrir no navegador

### 2. Personalizar o Logo
Para adicionar sua logo:
```html
<!-- No header, substitua: -->
<div class="logo">
    <div class="logo-text">
        <h1>ENGLISH <span class="highlight">FOREVER</span></h1>
        <div class="tagline">Transformando Oportunidades</div>
    </div>
</div>

<!-- Por: -->
<div class="logo">
    <img src="caminho/para/seu-logo.png" alt="English Forever Logo">
</div>
```

### 3. Alterar Imagens do Slider
Modifique as URLs das imagens na seção do slider:
```html
<img src="SUA-IMAGEM-AQUI.jpg" alt="Descrição da imagem">
```

---

## 📧 Configuração do Formulário

### ✅ Método Recomendado: Formspree (GRATUITO)

**Passos para ativar:**
1. Acesse https://formspree.io
2. Clique em "Sign up free"
3. Use o email: `englishforevernopt@gmail.com`
4. Confirme o email no inbox
5. Pronto! O formulário já funcionará

**Limite gratuito:** 50 submissões/mês

### 🔧 Método Alternativo: PHP

Crie um arquivo `send-email.php` no seu servidor:

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = htmlspecialchars($_POST['name']);
    $email = htmlspecialchars($_POST['email']);
    $phone = htmlspecialchars($_POST['phone']);
    $subject = htmlspecialchars($_POST['subject']);
    $service = htmlspecialchars($_POST['service']);
    $message = htmlspecialchars($_POST['message']);
    $language = htmlspecialchars($_POST['language']);
    
    $to = "englishforevernopt@gmail.com";
    $email_subject = "Novo contacto do site English Forever";
    
    $body = "Nome: $name\n";
    $body .= "Email: $email\n";
    $body .= "Telefone: $phone\n";
    $body .= "Assunto: $subject\n";
    $body .= "Serviço: $service\n";
    $body .= "Idioma: $language\n\n";
    $body .= "Mensagem:\n$message\n";
    
    $headers = "From: $email\r\n";
    $headers .= "Reply-To: $email\r\n";
    $headers .= "Content-Type: text/plain; charset=UTF-8\r\n";
    
    if (mail($to, $email_subject, $body, $headers)) {
        echo "success";
    } else {
        echo "error";
    }
}
?>
```

E altere o action do formulário para: `action="https://seusite.com/send-email.php"`

---

## 📱 Responsividade

O site foi otimizado para:
- **Desktop:** > 1200px
- **Tablet:** 768px - 1199px
- **Mobile:** < 767px

### Características mobile:
- Menu hamburguer
- Layout vertical
- Textos ajustados
- Imagens otimizadas

---

## 🎯 SEO e Performance

### ✅ Otimizações Incluídas:
- Meta tags para descrição e viewport
- Imagens com alt text descritivo
- HTML semântico (header, section, footer)
- Carregamento rápido (tudo em um arquivo)
- Navegação por âncoras suave

### 🔍 Para Melhorar SEO:
1. Adicionar meta description personalizada
2. Incluir Open Graph tags para redes sociais
3. Configurar Google Analytics
4. Criar sitemap.xml

---

## 📁 Estrutura do Código

```
index.html
├── HEADER (Logo + Menu + Idioma)
├── SLIDER (4 imagens com overlay)
├── SEÇÕES DE CONTEÚDO:
│   ├── Hero (CTA principal)
│   ├── Sobre Nós
│   ├── Cursos (4 cards)
│   ├── Tradução (2 serviços)
│   ├── Interpretação (3 serviços)
│   ├── Depoimentos (3 cards)
│   └── Contacto (Info + Formulário)
└── FOOTER (Links + Contacto + Social)
```

---

## 🔧 Personalização

### Cores (Variáveis CSS):
```css
:root {
    --dark-blue: #0a2463;    /* Azul escuro principal */
    --medium-blue: #1e3a8a;  /* Azul médio */
    --light-blue: #3b82f6;   /* Azul claro */
    --white: #ffffff;        /* Branco */
    --red: #e63946;          /* Vermelho de destaque */
    --light-gray: #f8f9fa;   /* Cinza claro para fundos */
    --dark-gray: #333333;    /* Cinza escuro para texto */
}
```

### Alterar Informações de Contacto:
- Telefones: +244 973 083 359 / +244 939150710
- Email: englishforevernopt@gmail.com
- Endereço: Lubango, Angola
- Horário: Seg-Sex 7h-19h15 | Sáb 8h-11h / 15h-17h10

---

## 🐛 Solução de Problemas

### Problema: Formulário não envia
**Solução:**
1. Verifique conexão com internet
2. Confirme email no Formspree
3. Verifique console do navegador (F12)

### Problema: Site não responsivo
**Solução:**
1. Adicione viewport tag
2. Verifique media queries
3. Teste em diferentes dispositivos

### Problema: Imagens não carregam
**Solução:**
1. Verifique URLs das imagens
2. Use imagens com tamanho otimizado
3. Use CDN ou hospedagem própria

---

## 📈 Próximos Passos Recomendados

1. **Hospedagem:** Netlify, Vercel ou GitHub Pages (gratuitos)
2. **Domínio:** Registrar `englishforever.co.ao`
3. **Google My Business:** Criar perfil para SEO local
4. **Analytics:** Instalar Google Analytics
5. **Backup:** Fazer backup regular do código

---

## 👥 Contribuição

Para contribuir com melhorias:
1. Faça fork do projeto
2. Crie uma branch (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Add nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

---

## 📄 Licença

Este projeto está disponível para uso da English Forever. Personalize conforme necessário para sua escola.

---

## 📞 Suporte

Para suporte técnico:
- Email: englishforevernopt@gmail.com
- WhatsApp: +244 973 083 359

---

**Desenvolvido com ❤️ para English Forever - Transformando Oportunidades Através do Inglês**