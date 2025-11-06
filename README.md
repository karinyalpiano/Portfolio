# Portfólio — Tema Dev (PT/EN) v3

**Correção principal:** o conteúdo em PT (incluindo **Sobre mim**) agora é a **fonte de verdade** no HTML. O script salva um _snapshot_ do texto original e **só traduz quando você alternar para EN**. Assim, editar o HTML atualiza imediatamente sem ser sobrescrito pelo i18n.

O que foi ajustado:
- i18n: snapshot do DOM (`data-i18n-original`) + traduções apenas para EN.
- Tema: toggle dark/light preservado (classe `dark` + variáveis CSS).
- Metas (description/og:description) sincronizadas por idioma.

Como editar o “Sobre mim”:
- Edite diretamente o parágrafo em `index.html` dentro da seção **SOBRE MIM** (PT). Não precisa mexer nas traduções, a menos que queira ajustar o texto em inglês.

Gerado em 2025-11-06 14:18 UTC.
