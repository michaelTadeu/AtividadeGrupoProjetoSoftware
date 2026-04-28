# Redesign da Página de Bolsas e Auxílios

## Resumo

Redesign completo da página `pagina_bolsas.html` com layout moderno e funcional, substituindo o accordion Bootstrap genérico por um design com cards, hero section com gradiente, ícones, animações e melhor hierarquia visual.

## Antes vs Depois

O layout antigo utilizava um simples accordion Bootstrap com fundo branco e sem diferenciação visual entre os tipos de auxílio. O novo design traz:

## Screenshots do Resultado

### Topo da Página
![Topo da página redesenhada](C:\Users\Aryane\.gemini\antigravity\brain\4a48dd10-e253-4c69-8bf4-72ed9ec1ab9d\bolsas_page_top_1777417898664.png)

### Parte Inferior
![Parte inferior da página redesenhada](C:\Users\Aryane\.gemini\antigravity\brain\4a48dd10-e253-4c69-8bf4-72ed9ec1ab9d\bolsas_page_bottom_1777417902379.png)

## Gravação da Navegação
![Demonstração da página no browser](C:\Users\Aryane\.gemini\antigravity\brain\4a48dd10-e253-4c69-8bf4-72ed9ec1ab9d\bolsas_screenshot_verify_1777417878150.webp)

## Arquivos Modificados

### [MODIFY] [pagina_bolsas.html](file:///c:/Users/Aryane/OneDrive/Documentos/Repositorios/AtividadeGrupoProjetoSoftware/pagina_bolsas.html)

Redesign completo com:
- **Hero Section**: Gradiente verde institucional com badge "Oportunidades", título grande, descrição e 3 estatísticas (5 Tipos de Auxílio, 100+ Alunos Beneficiados, 2025 Editais Abertos)
- **5 Cards de Auxílio** (Permanência, Alimentação, Transporte, Moradia, Didático): Cada card tem ícone colorido, descrição expandida, links para edital e formulário, e tag "Aberto"
- **Seção de Informações**: 3 mini-cards (Prazos, Documentação, Dúvidas)
- **Animações**: Cards aparecem com fade-in ao rolar (IntersectionObserver)
- **SEO**: Meta description, hierarquia semântica `<section>`, IDs únicos
- **Bootstrap Icons** para ícones visuais
- **Google Fonts Inter** para tipografia moderna

### [NEW] [bolsas.css](file:///c:/Users/Aryane/OneDrive/Documentos/Repositorios/AtividadeGrupoProjetoSoftware/bolsas.css)

CSS dedicado com:
- Design system com variáveis CSS (`--accent` por card)
- Gradiente hero com efeitos radiais decorativos
- Cards com hover lift (translateY + shadow)
- Ícones com `color-mix()` para backgrounds dinâmicos
- Layout responsivo (mobile-first breakpoints)
- Micro-animações em links e botões

## Melhorias Visuais Implementadas

| Aspecto | Antes | Depois |
|---------|-------|--------|
| Layout | Accordion genérico | Cards com ícones e cores individuais |
| Tipografia | Arial padrão | Inter (Google Fonts) |
| Cores | Verde Bootstrap padrão | Gradientes + cores por categoria |
| Ícones | Nenhum | Bootstrap Icons em cada card |
| Animações | Nenhuma | Fade-in on scroll, hover effects |
| Responsividade | Básica | Breakpoints otimizados |
| Hierarquia | Títulos iguais | Hero + Cards + Info section |

## Verificação

- ✅ Página carrega corretamente no browser
- ✅ CSS externo carrega sem erros
- ✅ Bootstrap Icons renderizam
- ✅ Animações de scroll funcionam
- ✅ Layout responsivo
- ✅ Menu lateral preservado e consistente com outras páginas
