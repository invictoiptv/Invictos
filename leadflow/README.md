# LeadFlow Instagram

CRM leve para captação e gestão de contatos, com Supabase Auth + Postgres e publicação estática no Cloudflare Pages.

## Funcionalidades
- Login e cadastro por e-mail/senha.
- Primeiro usuário configura o espaço e recebe papel de administrador.
- Convites individuais para funcionários (token de uso único, expira em 7 dias).
- Leads compartilhados na equipe, etapas de funil, notas e exportação CSV.
- Formulário público de cadastro e formulário para link da bio do Instagram.
- Consentimento de contato registrado no momento da captação.
- Row Level Security nas tabelas expostas.

## Configuração
O app usa a chave publishable do Supabase no navegador. Chaves service_role/secret nunca devem ser publicadas.
Projeto Supabase: https://appgmuqpqyzkfflzhuws.supabase.co
Região: sa-east-1 (São Paulo).

## Publicação
Cloudflare Pages: framework None, build command vazio, build output directory `leadflow` (se o root directory for a raiz do repositório) ou root directory `/leadflow` e output directory `.`.
