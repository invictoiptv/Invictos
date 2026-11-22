# LeadFlow Instagram

CRM de prospecção e gestão de contatos, com Supabase Auth + Postgres e publicação estática no Cloudflare Pages.

## Central de prospecção
- Pesquisa por @ de perfil, hashtags, localização e URLs de publicações em páginas públicas indexadas.
- Localização de telefones e e-mails publicados em páginas encontradas, com link da fonte e revisão humana antes de salvar.
- Importação CSV de listas de seguidores/seguindo obtidas legitimamente pelo titular da conta ou por fonte autorizada.
- Histórico de pesquisas e importações compartilhado dentro do espaço de trabalho.
- Cadastro manual, deduplicação, exportação CSV e qualificação de contatos.
- Separação entre empresas (contato comercial publicado) e pessoas físicas (consentimento, inbound ou relacionamento pré-existente).

## Limites e privacidade
A API oficial do Instagram/Meta não fornece a lista completa de seguidores ou seguindo de perfis de terceiros, nem os telefones privados dessas pessoas. A ferramenta não faz scraping autenticado, não contorna limites da plataforma e não apresenta perfis encontrados em pesquisa pública como se fossem seguidores.
A pesquisa de URLs de publicações pode encontrar páginas indexadas, mas não equivale a extrair todos os comentaristas. Para seguidores, seguindo e listas de comentaristas, use somente exportações ou fontes às quais o titular tenha acesso legítimo e importe os dados com base válida.
Telefones/e-mails identificados em páginas públicas são candidatos; a equipe deve conferir se a própria empresa divulga aquele canal para atendimento comercial antes de salvar ou contatar. Pessoas físicas exigem consentimento, solicitação de contato ou outra base legal válida. Respeite pedidos de interrupção de contato e mantenha a origem dos dados.

## Segurança e dados
- Supabase Auth e Row Level Security.
- Histórico de prospecção isolado por workspace.
- A chave publishable pode estar no navegador; chaves service_role/secret nunca devem ser publicadas.
- WhatsApp abre conversas individuais para revisão humana; não há disparo automático.

## Infraestrutura
Supabase: https://appgmuqpqyzkfflzhuws.supabase.co (sa-east-1).
Cloudflare Pages: projeto `leadflow-instagram`.
GitHub: `invictoiptv/Invictos`, branch `leadflow-instagram`.
