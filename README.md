# Portfólio Pessoal - Felipe Vieira Rodrigues

## Descrição do Projeto
Este é um portfólio pessoal simples, responsivo e moderno, desenvolvido para apresentar o perfil profissional de Felipe Vieira Rodrigues, estudante de Análise e Desenvolvimento de Sistemas. O site inclui seções principais como "Início" (com bio e foto de perfil), "Projetos" (galeria de projetos pessoais) e "Contato" (formulário integrado com EmailJS para envio direto de mensagens).

Recursos destacados:
- Design clean com navegação suave via âncoras HTML.
- Seção de projetos com grid responsivo e imagens ilustrativas.
- Formulário de contato que captura nome, e-mail, mensagem e timestamp, enviando via EmailJS sem necessidade de backend.
- Links para redes sociais (LinkedIn e GitHub).
- Responsivo para dispositivos móveis, com transições CSS e efeitos de hover.

O foco é demonstrar habilidades em desenvolvimento web front-end, integração de serviços externos e boas práticas de UX/UI. O site é estático e pode ser hospedado em plataformas como GitHub Pages.

## Tecnologias Utilizadas
- **HTML5**: Estrutura semântica, com elementos como `<header>`, `<nav>`, `<section>` e `<form>` para acessibilidade e SEO.
- **CSS3**: Estilos personalizados com Flexbox , CSS Grid e media queries implícitas para responsividade. Cores principais: #1e1e2f (azul escuro), #00bcd4 (azul claro para hover), #f4f4f9 (fundo claro).
- **JavaScript (Vanilla)**: Manipulação de eventos no formulário (preventDefault, FormData), integração com EmailJS para envio de e-mails, captura de data/hora local e logs no console para depuração.
- **EmailJS**: Biblioteca para envio de e-mails do front-end (SDK v4 via CDN). Configurado com Service ID (`service_Felipe`), Template ID (`template_178rj6o`) e Public Key (`q2Y8_OS4E2r0irjoj`).
- **Outras Ferramentas**: 
  - Imagens locais em JPEG (ex: `img/ATV port.jpeg` para perfil, `img/Componentes.jpeg` para projeto).
  - Hospedagem: GitHub Pages para publicação estática.
  - Sem frameworks pesados; foco em vanilla para simplicidade e performance.

O site é otimizado para navegadores modernos (Chrome, Firefox, etc.) e não requer dependências externas além do EmailJS.

## Instruções para Configurar o EmailJS
O formulário de contato utiliza o EmailJS para enviar mensagens diretamente para o e-mail do desenvolvedor (felipevieirar@yahoo.com.br) sem servidor backend. Para configurar ou clonar o projeto:

1. **Crie uma Conta no EmailJS**:
   - Vá para [www.emailjs.com](https://www.emailjs.com/) e registre-se gratuitamente.
   - Conecte um provedor de e-mail (ex: Gmail ou Yahoo) no dashboard.

2. **Crie o Serviço de E-mail**:
   - No dashboard, adicione um novo "Email Service" (ex: nomeie como "Meu Serviço de Contato").
   - Copie o **Service ID** gerado (ex: `service_Felipe` no código atual).
   - No arquivo `index.html`, substitua na linha do script: `emailjs.sendForm('service_Felipe', ...)` pelo seu Service ID.

3. **Crie o Template de E-mail**:
   - Adicione um novo "Email Template" com variáveis como `{{user_name}}`, `{{user_email}}`, `{{message}}` e `{{time}}`.
   - Exemplo de conteúdo: "Nova mensagem recebida em {{time}} de {{user_name}} ({{user_email}}): {{message}}".
   - Copie o **Template ID** (ex: `template_178rj6o` no código).
   - Atualize no script: `emailjs.sendForm('service_Felipe', 'template_178rj6o', this)`.

4. **Obtenha a Chave Pública**:
   - No dashboard > "Account" > "API Integration" > "Public Key", copie a chave (ex: `q2Y8_OS4E2r0irjoj`).
   - Substitua no script de inicialização: `emailjs.init("q2Y8_OS4E2r0irjoj");`.

5. **Inclua o SDK no HTML**:
   - Mantenha o script no `<head>`:  
     `<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>`

6. **Teste a Configuração**:
   - Abra o `index.html` no navegador e preencha o formulário.
   - Verifique o console (F12) para logs de envio ou erros.
   - Limite gratuito: 200 e-mails/mês. Para erros, confira alertas no código (ex: fallback para e-mail direto).
   - **Segurança**: Use apenas a Public Key no front-end; evite expor chaves privadas. Consulte a [documentação do EmailJS](https://www.emailjs.com/docs/) para mais opções.

Após configuração, o formulário enviará e-mails com sucesso e resetará automaticamente.

## Link para o Site Publicado
O site está hospedado no GitHub Pages e pode ser acessado em:  
https://felipevieirarodrigues.github.io/Portifolio-AV1  

## Como Executar Localmente
1. **Clone ou Baixe o Repositório**:
   - No GitHub: `git clone https://github.com/FelipeVieiraRodrigues/portfolio.git` (substitua pelo link real do seu repositório).
   - Ou baixe o ZIP e extraia.

2. **Estrutura de Arquivos**:
   - `index.html`: Arquivo principal.
   - Pasta `img/`: Contendo `ATV port.jpeg` (foto de perfil) e `Componentes.jpeg` (imagem do projeto).

3. **Abra no Navegador**:
   - Abra `index.html` diretamente no navegador (ex: Chrome ou Firefox).
   - Para testar o formulário, configure o EmailJS como acima.

4. **Publicar no GitHub Pages**:
   - Crie um repositório público no GitHub (ex: "portfolio").
   - Faça commit e push dos arquivos.
   - Vá em Settings > Pages > Source: "Deploy from a branch" > Selecione "main" > Save.
   - O site estará disponível em `https://seu-usuario.github.io/nome-do-repo`.

## Contato e Contribuições
Para dúvidas ou sugestões, use o formulário no site ou contate via:
- E-mail: felipevieirar@yahoo.com.br
- LinkedIn: [Felipe Vieira Rodrigues](https://www.linkedin.com/in/felipe-vieira-undefined-565800301)
- GitHub: [FelipeVieiraRodrigues](https://github.com/FelipeVieiraRodrigues)

Sinta-se à vontade para fork e contribuir com melhorias!

&copy; 2025 Felipe Vieira Rodrigues. Todos os direitos reservados.
